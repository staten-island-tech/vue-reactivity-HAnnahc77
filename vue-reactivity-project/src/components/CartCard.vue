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
  padding: 20px;
  text-align: center;
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-start;
  gap: 20px;
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
