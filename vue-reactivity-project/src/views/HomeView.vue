<template>
  <main>
    <div class="albumCards">
      <AlbumCard v-for="album in AlbumArray" :key="album.name" :album />
    </div>
  </main>
  <div></div>
</template>

<script setup>
import { AlbumArray } from '../assets/AlbumArray'
import AlbumCard from '../components/AlbumCard.vue'
</script>

<style scoped>
.albumCards {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  gap: 10px;
}
</style>
