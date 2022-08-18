<script setup>
import Home from './components/Home.vue'
import Navbar from './components/Navbar.vue'
</script>

<template>
  <Navbar />
  <div class="container">
    <Home />
  </div>
</template>

<style scoped>
.container {
  width: 90%;
  /* max-width: 1100px; */
  margin: 50px auto;
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  z-index: 999;
}
</style>
