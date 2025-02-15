<script setup>
import { defineAsyncComponent } from "vue";
// Import Components Asynchronously
const Navbar = defineAsyncComponent(() => import("@/components/NavBar.vue"));
const HeroSection = defineAsyncComponent(() =>
  import("@/components/HeroSection.vue")
);
const ServicesSection = defineAsyncComponent(()=>import('@/components/ServicesSection.vue'));
</script>

<template>
  <div class="bg-[#111827] min-h-screen">
    <Navbar />
    <HeroSection />
    <ServicesSection />
  </div>
</template>
