<template>
  <main>
    <div class="cartCards">
      <CartCard v-for="album in AlbumInCartArray" :key="album.name" :album="album" />
      <h2 v-if="AlbumInCartArray.length > 0">Total:{{ calcTotal(AlbumInCartArray) }}</h2>
    </div>
  </main>
</template>

<script setup>
import { AlbumInCartArray } from '../assets/AlbumArray'
import CartCard from '../components/CartCard.vue'

function calcTotal(AlbumInCartArray) {
  let total = 0
  AlbumInCartArray.forEach((album) => {
    total += album.price
  })
}
</script>

<style scoped>
.cardCards {
  align-items: center;
  justify-content: space-around;
}
</style>
