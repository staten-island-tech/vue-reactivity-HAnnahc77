<template>
  <main>
    <div class="cartCards">
      <button class="refresh" @click="reloadCart">Reset Cart</button>
      <CartCard v-for="album in ItemsInCart" :key="album.name" :album="album" />
      <h2 class="bg-white" v-if="ItemsInCart.length > 0">Total: ${{ totalPrice }}</h2>
    </div>
  </main>
</template>

<script setup>
import { computed, ref } from 'vue';
import { AlbumInCartArray } from '../assets/AlbumArray'; 
import CartCard from '../components/CartCard.vue';

const ItemsInCart = ref(AlbumInCartArray); 

function reloadCart(){
  ItemsInCart.value.length = 0;
}

const totalPrice = computed(() => {
  const total = ItemsInCart.value.reduce((totalPrice, item) => totalPrice + item.price, 0);
  return total.toFixed(2); 
});
</script>

<style scoped>
.cartCards {
  align-items: center;
  justify-content: space-around;
}

h2 {
  color: white;
}

.refresh {
  background-color: #a1c2e4;
  color: #181818;
  font-size: 16px;
  padding: 10px 20px;
  border-radius: 5px;
  border: 0;
  left: 50%;
}

.refresh:hover {
  background-color: white;
}
</style>
