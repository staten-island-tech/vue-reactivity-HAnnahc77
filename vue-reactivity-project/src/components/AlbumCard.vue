<template>
  <div class="albumCard">
    <h2>{{ album.name }}</h2>
    <img :src="album.img" :alt="album.name" />
    <h3>{{ album.price }}</h3>
    <h3>Created by: {{ album.band }}</h3>
    <button class="addToCart">Add to cart</button>
  </div>
</template>

<script setup>
defineProps({
  album: Object,
})
</script>

<style scoped>
.albumCard {
  width: 300px;
  box-sizing: border-box;
  border-radius: 8px;
  background-color: #f0f0f0;
  border: 1px solid black;
  padding: 16px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

.addToCart {
}
</style>
