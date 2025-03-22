<template>
  <Transition
    appear
    enter-from-class="opacity-0"
    leave-to-class="opacity-0"
    enter-active-class="transition ease-out duration-1000 delay-450"
    leave-active-class="transition ease-in duration-1000"
    enter-to-class="opacity-100"
    leave-from-class="opacity-100"
  >
    <section class="pt-20">
      <h2 class="mb-8 text-3xl font-extrabold">projects</h2>
      <div>
        <div
          v-for="project in Projects"
          :key="project.id"
          class="mb-20 grid items-center gap-8 opacity-90 transition duration-300 hover:-translate-y-1.5 hover:opacity-100 sm:grid-cols-2 sm:gap-12"
        >
          <div class="overflow-hidden rounded-md">
            <img
              :src="project.imagePath"
              alt="screenshot of mythology studio landing page"
            />
          </div>
          <div>
            <div class="mb-4 flex items-center justify-between">
              <h3 class="text-2xl font-extrabold">{{ project.name }}</h3>
              <div class="flex gap-4">
                <a
                  class="hover:text-mossGreen flex gap-1 transition hover:-translate-y-0.5"
                  :href="project.demoLink"
                  target="_blank"
                >
                  <Icon icon="gg:screen" width="24" height="24" />
                  <span>demo</span>
                </a>
                <a
                  class="hover:text-mossGreen flex gap-1 transition hover:-translate-y-0.5"
                  :href="project.repoLink"
                  target="_blank"
                >
                  <Icon icon="mingcute:github-line" width="24" height="24" />
                  <span>repo</span>
                </a>
              </div>
            </div>
            <div class="mb-8 flex items-center gap-2">
              <span
                v-for="(skill, index) in project.tech"
                :key="index"
                class="rounded-md border px-2 text-sm"
                :class="tagColors[skill]"
                >{{ skill }}</span
              >
            </div>
            <p>
              {{ project.description }}
            </p>
          </div>
        </div>
      </div>
    </section>
  </Transition>
</template>

<script setup>
import { Icon } from "@iconify/vue/dist/iconify.js";
import Projects from "../projects.json";
import { computed } from "vue";

const tagColors = {
  vuejs: "text-mossGreen",
  nuxtjs: "text-mossGreen",
  gsap: "text-orangeGold",
  css: "text-orangeGold",
  tailwindcss: "text-orangeGold",
  typescript: "text-vermillion",
  javascript: "text-vermillion",
};
</script>
