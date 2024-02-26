<template>
    <div class="gamecard">
        <h2>{{ Game.name }}</h2>
        <h2>{{ Game.price }}</h2>
    <img :src = "Game.img" alt="" />
    <button @click = "increment">Add to Cart</button>
    </div>
</template>

<script setup>
const props = defineProps({
    Game: Object,
});
</script>

<style scoped>
img {
width: 50%;
height: 10rem;
}

.gamecard {
  width: 22%;
  background-color: var(--secondary);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
  border-radius: 1rem;
  margin: 25px 25px;
  box-shadow: 1rem 1rem 0.5rem var(--tertiary);
  transition: all 0.3s ease-in-out;
  padding-bottom: 40px;
}
</style>