<template>
  <header>
    <div class="header">
      <nav>
        <RouterLink to="/">Items</RouterLink>
        <RouterLink to="/cart">Cart</RouterLink>
      </nav>
    </div>
  </header>
  <RouterView />
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<style scoped>
.header {
  position: absolute;
  top: 0;
  left: 0;
  font-size: 40px;
}
</style>
