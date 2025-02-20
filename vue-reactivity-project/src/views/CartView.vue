<template>
  <main>
    <div class="cartCards">
      <CartCard v-for="album in AlbumInCartArray" :key="album.name" :album="album" />
      <h2 class="bg-white" v-if="AlbumInCartArray.length > 0">Total: ${{ sumWithInitial }}</h2>
    </div>
  </main>
</template>

<script setup>
import { computed } from 'vue';
import { AlbumInCartArray } from '../assets/AlbumArray'; 
import CartCard from '../components/CartCard.vue';

const sumWithInitial = computed(() => {
  const total = AlbumInCartArray.reduce((accumulator, currentValue) => accumulator + currentValue.price, 0);
  return total.toFixed(2); 
});
</script>

<style scoped>
.cartCards {
  align-items: center;
  justify-content: space-around;
}

h2 {
  color: black;
}
</style>
