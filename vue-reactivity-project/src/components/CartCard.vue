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
  border-radius: 10px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  padding: 20px;
  width: 100%;
  max-width: 100%;
  margin-bottom: 20px;
  transition: all 0.3s ease;
}

.cartCard:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
}

.cartCard h2 {
  font-size: 1.5em;
  font-weight: 600;
  color: #333;
  margin: 10px 0;
}

.cartCard h3 {
  font-size: 1.2em;
  color: #777;
  margin: 5px 0;
}

.cartCard h2:last-of-type {
  font-size: 1.4em;
  font-weight: 600;
  color: #e74c3c;
  margin-top: 10px;
}

.cartCard h2,
.cartCard h3 {
  margin: 0;
}
</style>
