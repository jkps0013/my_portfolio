<template>
  <section class="text-white mt-20" id="projects">
    <div class="px-4 xl:pl-16">
      <!-- Section Title -->
      <div class="mb-8 md:flex md:justify-between xl:pr-16">
        <h2 class="text-4xl font-extrabold text-white mb-4">
          My Latest Achievements
        </h2>
      </div>

      <!-- Projects Grid -->
      <ul
        class="px-4 sm:py-16 xl:pr-16 grid grid-cols-1 gap-8 pt-10 sm:grid-cols-2 md:gap-10 md:pt-12 lg:grid-cols-3"
        data-aos="fade-right"
      >
        <li
          v-for="project in Projects"
          :key="project.id"
          class="rounded-lg overflow-hidden shadow-lg bg-[#111a3e] border border-[#1f1641] group hover:scale-[1.03] transition-transform duration-300"
        >
          <!-- Image Container -->
          <div
            class="h-52 md:h-64 flex items-center justify-center bg-[#181818] relative"
          >
            <img
              v-lazy="project.image"
              alt="Project Image"
              class="max-h-full max-w-full object-contain"
            />
            <div
              class="overlay absolute top-0 left-0 w-full h-full flex items-center justify-center bg-[#111a3e] bg-opacity-0 group-hover:bg-opacity-90 transition-all duration-300"
            >
              <a
                class="h-14 w-14 flex items-center justify-center rounded-full border-2 border-[#ADB7BE] hover:border-white transition-colors duration-300"
                :href="project.webURL"
                target="_blank"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke-width="1.5"
                  stroke="currentColor"
                  aria-hidden="true"
                  class="h-8 w-8 text-[#ADB7BE] group-hover:text-white"
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

          <!-- Text Content -->
          <div class="py-6 px-4">
            <h3 class="text-xl font-semibold uppercase text-white mb-2">
              {{ project.title }}
            </h3>
            <p class="text-[#ADB7BE] text-sm leading-relaxed">
              {{ project.description }}
            </p>
          </div>
        </li>
      </ul>
    </div>
  </section>
</template>
  
  <script setup>
import { ref } from "vue";
import ipImage from "@/assets/ip.jpeg";
import siemensLogo from "@/assets/siemens_LOGO.jpeg";
import shapeImage from "@/assets/shape.jpeg";
const Projects = ref([
  {
    id: 1,
    category: "IP Samman certificate",
    image: ipImage ,
    title: "Award",
    description:
      "Received IP Samman certificate under the category Rising Inventor from Siemens Technology and Service PVT LTD.",
    webURL:
      "https://drive.google.com/file/d/1b0uCjrMmfQeW-mLZiI9Lcu7KsD2SdGu4/view?usp=sharing",
  },
  {
    id: 2,
    category: "Got an idea archived for Siemens",
    image: siemensLogo,
    title: "Idea Archival",
    description: "Archived an idea for Siemens Technology and Service PVT LTD.",
    webURL:
      "https://drive.google.com/file/d/17l4gEczpxc0NNeb0lvGhFIIjmH4TmLIG/view",
  },
  {
    id: 3,
    category: "Contribution for Shape AI Community",
    image: shapeImage,
    title: "Contribution for Shape AI Community",
    description:
      "Made contributions to the Shape AI community by creating a project on the topic of Web Development.",
    webURL:
      "https://drive.google.com/file/d/1Iiga8s-hyTUnr0OepJIVsuRxksAstzi7/view",
  },
]);
</script>
  
  <style>
.overlay {
  display: none;
}

.group:hover .overlay {
  display: flex;
}
</style>
  