<template>
  <main>
    <div class="cartCards">
      <CartCard v-for="album in AlbumInCartArray" :key="album.name" :album="album" />
    </div>
  </main>
</template>

<script setup>
import { AlbumInCartArray } from '../assets/AlbumArray'
import CartCard from '../components/CartCard.vue'
</script>

<style scoped>
.cardCards {
  display: flex;
  flex-flow: row wrap;
  align-items: center;
  justify-content: space-around;
}
</style>
