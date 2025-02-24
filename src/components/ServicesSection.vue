<template>
  <section class="text-white mt-20" id="services">
    <div class="px-4 xl:pl-16">
      <h2 class="text-4xl font-bold text-white mb-4">My Services</h2>
    </div>
    <div
      class="py-8 xl:px-16 px-4 sm:py-16 grid grid-cols-1 gap-6 pt-10 sm:grid-cols-2 md:gap-10 md:pt-12 lg:grid-cols-3"
    >
      <div
        v-for="service in services"
        :key="service.id"
        data-aos="fade-up"
        class="px-8 py-12 rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641]"
      >
        <div class="mx-auto h-24 w-24 text-center xl:h-28 xl:w-28">
          <div>
            <img :src="service.icon" alt="service icon" />
          </div>
        </div>
        <div class="text-center">
          <h3
            class="pt-8 text-lg font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-[#f59e0b] to-[#ec4899] lg:text-xl"
          >
            {{ service.name }}
          </h3>
          <p class="pt-4 text-grey text-sm group-hover:text-white md:text-base">
            {{ service.description }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";
const services = ref([
  {
    id: 1,
    icon: "https://img.icons8.com/pastel-glyph/100/ffffff/laptop-coding--v1.png",
    name: "WEB DEVELOPMENT",
    description: "Building responsive, fast, and user-friendly websites.",
  },
  {
    id: 2,
    icon: "https://img.icons8.com/external-prettycons-lineal-prettycons/100/ffffff/external-mobile-development-ui-mobile-prettycons-lineal-prettycons.png",
    name: "Mobile Development",
    description: "Creating smooth, high-performance mobile applications.",
  },
  {
    id: 3,
    icon: "https://img.icons8.com/external-solidglyph-m-oki-orlando/100/ffffff/external-website-maintenance-seo-solid-solidglyph-m-oki-orlando.png",
    name: "Website Maintenance",
    description:
      "Offer ongoing support and updates to ensure websites run smoothly and securely.",
  },
  {
    id: 4,
    icon: "https://img.icons8.com/ios/100/ffffff/database--v1.png",
    name: "Backend Services",
    description:
      "develop and manage backend systems, ensuring efficient data handling, server-side operations, and secure API integration.",
  },
  {
    id: 5,
    icon: "https://img.icons8.com/ios-filled/100/ffffff/windows10-personalization.png",
    name: "Frontend Services",
    description:
      "Create user-friendly, responsive, and visually appealing interfaces across all devices.",
  },
  {
    id: 6,
    icon: "https://img.icons8.com/ios-filled/100/ffffff/github.png",
    name: "Version Control with Git",
    description:
      "Use Git for efficient version control, enabling seamless collaboration and code management.",
  },
]);
</script>
