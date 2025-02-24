<template>
  <section class="text-white mt-20 min-h-[450px]" id="projects">
    <div class="px-4 xl:pl-16">
      <div class="mb-4 md:flex md:justify-between xl:pr-16">
        <h2 class="text-4xl font-bold text-white">My Latest Projects</h2>
        <div class="flex space-x-4 mb-4 mt-5 md:mt-0">
          <button
            v-for="category in ['All', 'Web Development', 'Mobile App']"
            class="hover:text-[#f59e0b] transition ease-in-out z-10 cursor-pointer duration-300"
            :key="category"
            @click="() => (selectedCategory = category)"
          >
            {{ category }}
          </button>
        </div>
      </div>
      <ul
        class="px-4 sm:py-16 xl:pr-16 grid grid-cols-1 gap-6 pt-10 sm:grid-cols-2 md:gap-10 md:pt-12 lg:grid-cols-3"
        data-aos="fade-right"
      >
        <template v-if="filteredProjects.length > 0">
          <div v-for="project in filteredProjects" :key="project.id">
            <div
              class="h-52 md:h-[24rem] rounded-t-xl relative group"
              :style="{
                backgroundImage: 'url(' + project.image + ')',
                backgroundSize: 'cover',
              }"
            >
              <div
                class="overlay transition-all duration-500 items-center justify-center absolute top-0 left-0 w-full h-full bg-[#181818] opacity-0 hidden group-hover:flex group-hover:opacity-80"
              >
                <a
                  class="h-14 w-14 mr-2 border-2 relative rounded-full border-[#ADB7BE] hover:border-white group/link"
                  :href="project.gitURL"
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke-width="1.5"
                    stroke="currentColor"
                    aria-hidden="true"
                    data-slot="icon"
                    class="h-10 w-10 text-[#ADB7BE] absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 cursor-pointer group-hover/link:text-white"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M17.25 6.75 22.5 12l-5.25 5.25m-10.5 0L1.5 12l5.25-5.25m7.5-3-4.5 16.5"
                    ></path>
                  </svg>
                </a>
                <a
                  class="h-14 w-14 border-2 relative rounded-full border-[#ADB7BE] hover:border-white group/link"
                  :href="project.webURL"
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke-width="1.5"
                    stroke="currentColor"
                    aria-hidden="true"
                    data-slot="icon"
                    class="h-10 w-10 text-[#ADB7BE] absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 cursor-pointer group-hover/link:text-white"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M2.036 12.322a1.012 1.012 0 0 1 0-.639C3.423 7.51 7.36 4.5 12 4.5c4.638 0 8.573 3.007 9.963 7.178.07.207.07.431 0 .639C20.577 16.49 16.64 19.5 12 19.5c-4.638 0-8.573-3.007-9.963-7.178Z"
                    ></path>
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M15 12a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z"
                    ></path>
                  </svg>
                </a>
              </div>
            </div>
            <div
              class="text-white rounded-b-xl mt-3 bg-[#111a3e] shadow-lg border border-[#1f1641] py-6 px-4"
            >
              <h3 class="text-lg font-semibold uppercase lg:text-xl">
                {{ project.title }}
              </h3>
              <p class="text-[#ADB7BE]">{{ project.description }}</p>
              <div class="flex flex-wrap py-2.5 gap-2">
                <div
                  v-for="technology in project.technologies"
                  :key="technology"
                  class="text-center rounded-2xl bg-[#111827] px-1.5"
                  style="
                    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
                    border: 1px solid #111827;
                    backdrop-filter: blur(9px);
                    -webkit-backdrop-filter: blur(9px);
                  "
                >
                  <p class="px-1 py-2">{{ technology }}</p>
                </div>
              </div>
            </div>
          </div>
        </template>

        <!-- ถ้าไม่มีโปรเจกต์ให้แสดงข้อความนี้ -->
        <p v-else class="text-white text-lg text-center col-span-full">
          No projects available
        </p>
      </ul>
    </div>
  </section>
</template>
<script setup>
import { ref, computed } from "vue";

const Projects = ref([
  {
    id: 1,
    category: "Web Development",
    image: "src/assets/MerryMatch.png",
    title: "Merry Match",
    description:
      "An engaging online dating platform designed to connect people through a seamless, user-friendly experience with an attractive and modern interface for all devices.",
    technologies: ["Next.js", "Node.js", "Express", "Supabase"],
    gitURL: "https://github.com/Teehim00/merry_match_project",
    webURL: "https://merry-match-project.vercel.app/",
  },
  {
    id: 2,
    category: "Web Development",
    image: "src/assets/PersonalBlog.png",
    title: "My Personal Blog",
    description:
      "A personal blog designed to share ideas, experiences, and inspiration through a clean and engaging reading experience. Users can log in to create and share their own posts.",
    technologies: ["React", "Tailwind CSS", "Express"],
    gitURL: "https://github.com/TongBud44/reangsak-personal-blog",
    webURL: "https://reangsak-personal-blog.vercel.app/",
  },
  {
    id: 3,
    category: "Web Development",
    image: "src/assets/MyPort.png",
    title: "My Port",
    description:
      "A portfolio website showcasing my web development projects, built with Vue.js and Tailwind CSS. Designed with a focus on responsive UI, clean code, and an intuitive user experience.",
    technologies: ["Vue.js", "Tailwind CSS"],
    gitURL: "https://github.com/TongBud44/my-portfolio",
    webURL: "",
  },
]);

const selectedCategory = ref("All");
const filteredProjects = computed(() => {
  if (selectedCategory.value === "All") {
    return Projects.value;
  }
  return Projects.value.filter(
    (project) =>
      project.category.toLocaleLowerCase() ===
      selectedCategory.value.toLocaleLowerCase()
  );
});
</script>
