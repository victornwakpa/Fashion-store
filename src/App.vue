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
  <div class="hero-bg flex gap-14 flex-col">
    <Navbar class="w-full px-24" />
    <Hero class="w-full px-24" />
  </div>
  <div>
    <BestSelling  class="w-full px-24"/>
    <OurProducts  class="w-full px-24" />
    <ExclusiveOffer class="w-full px-24" />
    <DesignerClothes class="w-full px-24" />
    <Feedback class="w-full px-24" />
    <Footer class="w-full px-24 btn-hero"/>
  </div>
</template>

<style scoped>

</style>
