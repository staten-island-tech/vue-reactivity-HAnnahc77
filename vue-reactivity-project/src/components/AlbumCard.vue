<template>
  <div class="albumCard">
    <h2>{{ album.name }}</h2>
    <img :src="album.img" :alt="album.name" />
    <h3>$ {{ album.price }}</h3>
    <h3>Created by: {{ album.band }}</h3>
    <button class="addToCart" @click="intoCart(album)">Add to cart</button>
    <h4 v-if="h4">Added!</h4>
  </div>
</template>

<script setup>
import { AlbumInCartArray } from '@/assets/AlbumArray'
import { ref } from 'vue'

defineProps({
  album: Object,
})
const h4 = ref(false)

function intoCart(album) {
  AlbumInCartArray.push(album)
  h4.value = true
  setTimeout(() => {
    h4.value = false
  }, 3000)
}
</script>

<style scoped>
.albumCard {
  width: 300px;
  border-radius: 12px;
  background-color: #181818;
  border: 1px solid #a1c2e4;
  padding: 20px 20px 50px 20px;
  text-align: center;
  position: relative;
}

h2 {
  font-size: 25.6px;
  color: white;
  margin-bottom: 10px;
}

h3 {
  font-size: 19.2px;
  color: white;
  margin: 5px;
}

h4 {
  font-size: 12.8px;
  color: white;
  margin-bottom: 5px;
}

img {
  width: 250px;
  height: 250px;
  object-fit: cover;
  border-radius: 8px;
}

.addToCart {
  background-color: #a1c2e4;
  color: #181818;
  font-size: 16px;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
  position: absolute;
  bottom: 20px;
  left: 50%;
  transform: translateX(-50%);
}

.addToCart:hover {
  background-color: white;
}

h4 {
  opacity: 1;
  transition:
    opacity 2s ease-out,
    visibility 0s 2s;
  padding-top: 2px;
  padding-bottom: 2px;
}

</style>
