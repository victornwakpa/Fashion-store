<script setup>
import Hero from './components/Hero.vue';
import Navbar from './components/Navbar.vue';
import BestSelling from './components/BestSelling.vue';
import OurProducts from './components/OurProducts.vue';
import ExclusiveOffer from './components/ExclusiveOffer.vue';
import DesignerClothes from './components/DesignerClothes.vue';
import Feedback from './components/Feedback.vue';
import Footer from './components/Footer.vue';
</script>

<template>
  <div class="flex gap-14 flex-col">
    <div class="" >
      <Navbar class="hero-bg w-full md:px-24" />
      <Hero class="hero-bg w-full md:px-24 px-8" />
      <BestSelling class="w-full md:px-24 px-8" />
      <OurProducts class="w-full md:px-24 px-8" />
      <ExclusiveOffer class="w-full md:px-24 px-8" />
      <DesignerClothes class="w-full md:px-24 px-8" />
      <Feedback class="w-full md:px-24 px-8" />
      <Footer class="w-full md:px-24 px-8 btn-hero" />
    </div>
    
  </div>
  <div>
    
  </div>
</template>

<style scoped>

</style>
