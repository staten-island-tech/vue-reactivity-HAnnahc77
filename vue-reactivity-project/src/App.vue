<template>
  <div class="container">
    <h1>Album Store</h1>
    <header>
      <div class="header">
        <nav>
          <RouterLink to="/">Albums</RouterLink>
          <RouterLink to="/cart">Cart</RouterLink>
        </nav>
      </div>
    </header>
    <RouterView />
  </div>
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Sigmar+One&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap');

body {
  font-family: 'Poppins', sans-serif;
} 

.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  height: 100vh;
  text-align: center;
  padding-top: 20px;
  background-color: #181818;
}

h1 {
  margin: 0;
  font-size: 3rem;
  color: white;
  font-family: 'Sigmar One', serif;
  font-style: normal;
}

.header {
  display: flex;
  justify-content: space-between;
  width: 100%;
  margin-top: 20px;
  padding: 0 20px;
  padding-bottom: 8px;
}

nav {
  display: flex;
  gap: 20px;
}

nav a {
  font-size: 19.2px;
  color: white;
}

nav a:hover {
  color: #007bff;
}
</style>
