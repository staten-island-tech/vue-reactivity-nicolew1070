<template>
    <div class="item">
        <h2>{{ item.name }}</h2>
        <h2>{{ item.price }}</h2>
        <img :src = "item.img" alt="" />
        <button @click="remove">Remove</button>
    </div>
</template>

<script>
import { store } from '../views/store.js'

export default {
    name: "CartArray",
    props: {
        item: Object,
        cart: Array,
    },
    methods: {
        remove() {
            store.cart.splice(this.index, 1);
        }
    }
}

</script>

<style scoped>
.item {
  background-color: var(--tertiary);
  flex-direction: column;
  align-items: center;
  justify-content: center;
  border-radius: 1rem;
  margin: 25px 25px;
  padding-bottom: 40px;
  }

  img {
  width: 50%;
  height: 10rem;
  margin-top: 1.5rem;
  }
</style>