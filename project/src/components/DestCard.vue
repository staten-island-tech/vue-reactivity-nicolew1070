<template>
    <div>
        <h2>{{ Game.name }}</h2>
        <h2>{{ Game.price }}</h2>
    <img :src = "Game.img" alt="" />
    </div>
</template>

<script setup>
const props = defineProps({
    Game: Object,
});
</script>

<style scoped>
img {
    width: 300px;
    height: 350px;
    object-fit: cover;
}
</style>