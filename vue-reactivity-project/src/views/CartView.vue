<template>
  <main>
    <div class="cartCards">
      <CartCard v-for="album in AlbumInCartArray" :key="album.name" :album />
    </div>
  </main>
</template>

<script setup>
import { AlbumInCartArray } from '../assets/AlbumArray'
</script>

<style scoped>
main {
  display: flex;
  justify-content: center;
  padding: 20px;
}

.cartCards {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 20px;
  width: 100%;
  max-width: 1200px;
}
</style>
