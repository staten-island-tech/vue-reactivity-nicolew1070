<template>
    <div class="gamecard">
        <h2>{{ Game.name }}</h2>
        <h2>{{ Game.price }}</h2>
    <img :src = "Game.img" alt="" />
    <button @click = "addToCart" class="btn">Add to Cart</button>
    </div>
</template>

<script setup>
import { store } from '@/stores/store';

const props = defineProps({
    Game: Object,
});

function addToCart() {
    store.cart.push(Game) 
};

</script>

<style scoped>
img {
width: 50%;
height: 10rem;
margin-top: 1.5rem;
}
.gamecard {
  width: 25%;
  background-color: var(--secondary);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
  border-radius: 1rem;
  margin: 25px 25px;
  box-shadow: 1rem 1rem 0.5rem var(--tertiary);
  padding-bottom: 40px;
}

.btn {
  background-color: var(--tertiary);
  padding: 0.5rem;
  font-size: 1.1rem;
  margin: 1rem auto;
  border: solid var(--primary);
}
</style>