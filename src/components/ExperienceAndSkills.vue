<template>
  <section class="text-white mt-18" id="skills">
    <div class="absolute right-0 top-[110rem] h-full w-full justify-end">
      <span class="flex opacity-20">
        <span
          class="w-16 h-32 rounded-l-full flex bg-[#f59e0b] blur-2xl"
        ></span>
        <span
          class="w-16 h-32 rounded-r-full flex bg-[#f88fc2] blur-2xl mt-14"
        ></span>
      </span>
    </div>

    <div
      class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-16 xl:px-16"
    >
      <div class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full w-[100%]">
        <h2 class="text-4xl font-bold text-white text-left mb-4">
          My
          <span
            class="text-transparent bg-clip-text bg-gradient-to-r from-[#f59e0b] to-[#ec4899]"
            >Skills</span
          >
        </h2>
        <div class="mt-8 grid grid-cols-3 lg:grid-cols-4">
          <div
            class="flex items-center justify-center p-4 flex-col lg:gap-4 gap-3"
            v-for="skill in Skills"
            :key="skill.id"
            data-aos="fade-right"
          >
            <img :src="skill.logo" alt="skill logo" />
            <h4 class="text-sm lg:text-xl font-semibold uppercase text-white">
              {{ skill.name }}
            </h4>
          </div>
        </div>
      </div>

      <div data-aos="flip-left" class="h-full">
        <h2
          class="text-4xl font-bold text-white text-left mb-8 md:text-center md:mt-0 mt-8"
        >
          My Experiences
        </h2>
        <div class="space-y-8 py-7" data-aos="fade-left">
          <div
            v-for="element in Experinces"
            :key="element.id"
            class="flex items-center rounded-xl p-4 bg-[#111a3e] shadow-lg border border-[#1f1641]"
          >
            <div class="w-1/4">
              <img
                src="https://img.icons8.com/ios-filled/90/ffffff/lawyer.png"
                alt="lawyer"
              />
            </div>
            <div class="w-3/4 pl-4">
              <h3
                class="sm:text-2xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-[#f59e0b] to-[#ec4899]"
              >
                {{ element.role }}
              </h3>
              <p class="text-white">{{ element.company }}</p>
              <p class="text-white">{{ element.date }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script setup>
import { ref } from "vue";
const Skills = ref([
  {
    id: 1,
    name: "HTmL",
    logo: "https://img.icons8.com/color/100/html-5--v1.png",
  },
  {
    id: 2,
    name: "CSS",
    logo: "https://img.icons8.com/color/100/css3.png",
  },
  {
    id: 3,
    name: "JavaScript",
    logo: "https://img.icons8.com/color/100/javascript--v1.png",
  },
  {
    id: 4,
    name: "SQL",
    logo: "https://img.icons8.com/external-soft-fill-juicy-fish/100/external-sql-coding-and-development-soft-fill-soft-fill-juicy-fish.png",
  },
  {
    id: 5,
    name: "React",
    logo: "https://img.icons8.com/office/100/react.png",
  },
  {
    id: 6,
    name: "Next.js",
    logo: "https://img.icons8.com/fluency-systems-regular/100/ffffff/nextjs.png",
  },
  {
    id: 7,
    name: "Vue.js",
    logo: "https://img.icons8.com/fluency/100/vuejs.png",
  },
  {
    id: 8,
    name: "node.js",
    logo: "https://img.icons8.com/fluency/100/node-js.png",
  },
  {
    id: 9,
    name: "express.js",
    logo: "https://img.icons8.com/office/100/express-js.png",
  },
  {
    id: 10,
    name: "mongoDB",
    logo: "https://img.icons8.com/color/100/mongo-db.png",
  },
  {
    id: 11,
    name: "Git",
    logo: "https://img.icons8.com/color/100/git.png",
  },
  {
    id: 12,
    name: "supabase",
    logo: "https://img.icons8.com/fluency/100/supabase.png",
  },
]);

const Experinces = ref([
  {
    id: 1,
    role: "Electrical Engineer",
    company: "Panel Plus Company Limited",
    date: "Nov 2023 - April 2024",
  },
  {
    id: 2,
    role: "Electrical Technician Internship",
    company: "Great Oriental Corporation Company Limited",
    date: "July 2022 - Nov 2022",
  },
]);
</script>
