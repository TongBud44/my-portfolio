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
const BackToTop = defineAsyncComponent(() =>
  import("@/components/BackToTop.vue")
);
import LoadingSpinner from "./components/LoadingSpinner.vue";
</script>

<template>
  <div class="bg-[#111827] min-h-screen">
    <Suspense>
      <template #default>
        <div>
          <Navbar />
          <HeroSection />
          <ServicesSection />
          <AboutSection />
          <ExperienceAndSkills />
          <ProjectSection />
          <ContactSection />
          <Footer />
          <BackToTop />
        </div>
      </template>
      <template #fallback>
        <div class="flex justify-center items-center min-h-screen">
          <LoadingSpinner />
        </div>
      </template>
    </Suspense>
  </div>
</template>

<style>
* {
  scrollbar-width: thin;
  scrollbar-color: #111827 #f1f1f1;
}
</style>
