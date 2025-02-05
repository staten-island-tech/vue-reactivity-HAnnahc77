<template>
  <main>
    <div class="albumCards">
      <AlbumCard v-for="album in AlbumInCartArray" :key="album.name" :album />
    </div>
  </main>
</template>

<script setup>
import { AlbumInCartArray } from '../assets/AlbumArray'
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
