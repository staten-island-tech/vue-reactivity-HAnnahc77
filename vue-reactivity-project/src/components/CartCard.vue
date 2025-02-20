<template>
  <div class="cartCard">
    <h2>{{ album.name }}</h2>
    <h2>$ {{ album.price }}</h2>
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
  padding: 20px;
  width: 900px;
  align-items: left;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.cartCard h2 {
  font-size: 1.5em;
  font-weight: 600;
  color: #333;
  margin: 10px 0;
}

.cartCard h2:last-of-type {
  font-size: 1.4em;
  font-weight: 600;
  color: #e74c3c;
  margin-top: 10px;
}
</style>
