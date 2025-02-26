<template>
  <section class="text-white mt-18" id="about">
    <div class="absolute z-0 top-[93rem] inset-x-0 h-64 flex items-start">
      <div
        class="h-24 w-64 bg-gradient-to-br from-[#f59e0b] via-[#ec4899] blur-2xl to-[#570cac] opacity-20"
      ></div>
    </div>
    <div
      class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-16 sm:py-16 xl:px-16 z-1"
    >
      <div data-aos="flip-right">
        <h2 class="text-4xl font-bold text-white text-left mb-8">
          My Education
        </h2>
        <div class="space-y-8 py-8">
          <div
            v-for="element in education"
            :key="element.id"
            class="flex items-center md:w-[80%] w-full rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] py-2"
          >
            <div class="w-1/4 pl-3">
              <img
                src="https://img.icons8.com/fluency-systems-regular/85/ffffff/education.png"
                alt="graduation-cap--v1"
              />
            </div>
            <div class="w-3/4 pl-4">
              <h3
                class="sm:text-2xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-[#f59e0b] to-[#ec4899] lg:text-xl"
              >
                {{ element.School }}
              </h3>
              <p class="text-white">{{ element.program }}</p>
              <p class="text-white">{{ element.year }}</p>
            </div>
          </div>
        </div>
      </div>
      <div
        class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full"
        data-aos="flip-right"
      >
        <h2 class="text-4xl font-bold text-white md:text-center text-left mb-4">
          More
          <span
            class="text-transparent bg-clip-text bg-gradient-to-r from-[#f59e0b] to-[#ec4899]"
            >About</span
          >
          Me
        </h2>
        <p class="text-base lg:text-lg mt-2 py-8">
          Hi, I'm Tong, a Fullstack Developer with a passion for building
          functional, scalable web applications. After transitioning from
          electrical engineering, I joined a Fullstack Developer Bootcamp to
          enhance my skills in Vue.js, React, Next.js, Node.js, and APIs. I
          focus on solving problems efficiently and creating user-friendly apps
          while continuously learning new technologies.
        </p>
        <div class="grid grid-cols-3 gap-4 lg:gap-10 max-w-auto pt-8">
          <div
            class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3"
          >
            <h3 class="text-white font-bold sm:text-2xl lg:text-3xl">
              Passionate
            </h3>
            <p class="text-sm sm:text-base text-gray-300">Learner 💡</p>
          </div>
          <div
            class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3"
          >
            <h3 class="text-white font-bold sm:text-2xl lg:text-3xl">
              +3
            </h3>
            <p class="text-sm sm:text-base text-gray-300">Projects 🖥️</p>
          </div>

          <div
            class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3"
          >
            <h3 class="text-white font-bold sm:text-2xl lg:text-3xl">
              5 Months
            </h3>
            <p class="text-sm sm:text-base text-gray-300">
              In Fullstack Development 👨🏻‍💻
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script setup>
import { ref } from "vue";
const education = ref([
  {
    id: 1,
    School: "TechUp Thialand",
    program: "Fullstack Developer Bootcamp",
    year: "2024 - 2025",
  },
  {
    id: 2,
    School: "Rajamangala University of Technology Srivijaya, Songkhla Campus",
    program: "Bachelor's degree in Electrical Engineering",
    year: "2019 - 2023",
  },
]);
</script>
