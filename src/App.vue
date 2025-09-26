<template>
  <div id="app">
    <!-- Navbar always at the top -->
    <Navbar />

    <!-- Main page content -->
    <router-view />

    <!-- Footer always at the bottom -->
    <Footer />
  </div>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import Footer from './components/Pooter.vue'
</script>

<style>
/* optional: make sure layout spans full height */
#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

router-view {
  flex: 1; /* push footer down */
}
</style>
