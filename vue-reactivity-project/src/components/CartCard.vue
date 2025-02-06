<template>
  <div class="cartCard">
    <h2>{{ album.name }}</h2>
    <h3>{{ album.band }}</h3>
    <h2>{{ album.price }}</h2>
  </div>
</template>

<script setup>
defineProps({
  album: Object,
})
</script>

<style scoped>
.cartCard {
  background-color: #fff;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  padding: 20px;
  text-align: center;
  transition: transform 0.3s ease;
}

.cartCard h2 {
  font-size: 1.5em;
  color: #333;
  margin: 10px 0;
}

.cartCard h3 {
  font-size: 1.2em;
  color: #666;
  margin: 5px 0;
}
</style>
