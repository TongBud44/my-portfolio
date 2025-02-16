<script setup>
import { defineAsyncComponent } from "vue";
// Import Components Asynchronously
const Navbar = defineAsyncComponent(() => import("@/components/NavBar.vue"));
const HeroSection = defineAsyncComponent(() =>
  import("@/components/HeroSection.vue")
);
const ServicesSection = defineAsyncComponent(() =>
  import("@/components/ServicesSection.vue")
);
const AboutSection = defineAsyncComponent(() =>
  import("@/components/AboutSection.vue")
);
const ExperienceAndSkills = defineAsyncComponent(() =>
  import("@/components/ExperienceAndSkills.vue")
);
const ProjectSection = defineAsyncComponent(() =>
  import("@/components/ProjectSection.vue")
);
const ContactSection = defineAsyncComponent(() =>
  import("@/components/ContactSection.vue")
);
const Footer = defineAsyncComponent(() => import("@/components/Footer.vue"));
</script>

<template>
  <div class="bg-[#111827] min-h-screen">
    <Navbar />
    <HeroSection />
    <ServicesSection />
    <AboutSection />
    <ExperienceAndSkills />
    <ProjectSection />
    <ContactSection />
    <Footer />
  </div>
</template>
