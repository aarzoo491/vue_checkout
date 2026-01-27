<script setup lang="ts">
import { RouterView } from 'vue-router'
import Navbar from './components/Navbar.vue'
</script>

<template>
  <Navbar />
  <main class="main-content">
    <RouterView />
  </main>
</template>

<style scoped>
:global(html) {
  height: auto;
}

:global(body) {
  width: 100%;
  height: auto;
  margin: 0;
  padding: 0;
}

:global(#app) {
  width: 100%;
  display: flex;
  flex-direction: column;
}

.main-content {
  width: 100%;
  flex: 1;
  background: #fff;
  overflow-x: hidden;
}
</style>
