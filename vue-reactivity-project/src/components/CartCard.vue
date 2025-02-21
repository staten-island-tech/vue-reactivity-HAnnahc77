<template>
  <div class="cartCard">
    <h2>{{ album.name }}</h2>
    <h2 class="price">$ {{ album.price }}</h2>
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
  width: 900px;
  align-items: left;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.cartCard h2 {
  font-size: 24px;
  font-weight: 600;
  margin: 10px 0;
}

.price {
  font-size: 22.4px;
  font-weight: 600;
  color: white;
  margin-top: 10px;
}
</style>
