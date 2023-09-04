<script setup>
import Hero from './components/Hero.vue';
import Navbar from './components/Navbar.vue';
import BestSelling from './components/BestSelling.vue';
</script>

<template>
  <div class="hero-bg flex gap-14 flex-col">
    <Navbar class="w-full px-24" />
    <Hero class="w-full px-24" />
  </div>
  <div>
    <BestSelling  class="w-full px-24"/>
  </div>
</template>

<style scoped>

</style>
