<template>
  <div class="albumCard">
    <h2>{{ album.name }}</h2>
    <img :src="album.img" :alt="album.name" />
    <h3>{{ album.price }}</h3>
    <h3>Created by: {{ album.band }}</h3>
  </div>
</template>

<script setup>
defineProps({
  album: Object,
})
</script>

<style scoped>
.albumCard {
  border-radius: 2px;
}
</style>
