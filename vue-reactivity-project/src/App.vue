<template>
  <div class="container">
    <h1>Store</h1>
    <header>
      <div class="header">
        <nav>
          <RouterLink to="/">Items</RouterLink>
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

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  height: 100vh;
  text-align: center;
  padding-top: 20px;
}

h1 {
  margin: 0;
  font-size: 3rem;
}

.header {
  display: flex;
  justify-content: space-between;
  width: 100%;
  max-width: 600px;
  margin-top: 20px;
  padding: 0 20px;
}

nav {
  display: flex;
  gap: 20px;
}

nav a {
  font-size: 1.2rem;
  color: #000;
}

nav a:hover {
  color: #007bff;
}
</style>
