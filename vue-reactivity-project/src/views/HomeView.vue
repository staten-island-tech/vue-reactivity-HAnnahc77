<template>
  <main>
    <AlbumCard v-for="album in AlbumArray" :key="album.name" :album />
  </main>
  <div></div>
</template>

<script setup>
import { AlbumArray } from '../assets/AlbumArray'
import AlbumCard from '../components/AlbumCard.vue'
</script>

<style scoped></style>
