<template>
  <div class="albumCard">
    <h2>{{ album.name }}</h2>
    <img :src="album.img" :alt="album.name" />
    <h3>{{ album.price }}</h3>
    <h3>Created by: {{ album.band }}</h3>
    <button class="addToCart" @click="intoCart">Add to cart</button>
    <h4 v-if="inCart">Added!</h4>
  </div>
</template>

<script setup>
import { AlbumInCartArray } from '@/assets/AlbumArray'
import { ref } from 'vue'

defineProps({
  album: Object,
})
const inCart = ref(false)

function intoCart(album) {
  AlbumInCartArray.push(album)
  inCart.value = !inCart.value
}
</script>

<style scoped>
.albumCard {
  width: 300px;
  box-sizing: border-box;
  border-radius: 12px;
  background-color: #fff;
  border: 1px solid #ddd;
  padding: 20px 20px 50px 20px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  text-align: center;
  transition: transform 0.3s ease-in-out;
  position: relative;
}

.albumCard:hover {
  transform: scale(1.05);
}

h2 {
  font-size: 1.6em;
  color: #333;
  margin-bottom: 10px;
}

h3 {
  font-size: 1.2em;
  color: #555;
  margin: 5px 0;
}

img {
  width: 250px;
  height: 250px;
  object-fit: cover;
  object-position: center;
  border-radius: 8px;
  margin: 0 auto 15px;
  display: block;
}

.addToCart {
  background-color: #000000;
  color: white;
  font-size: 1em;
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
  background-color: #a1c2e4;
}

h4 {
  opacity: 0;
  transition: opacity 0.5s ease-in-out;
}

.show {
  opacity: 1;
  animation: showFor3Seconds 3s forwards;
}

@keyframes showFor3Seconds {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}
</style>
