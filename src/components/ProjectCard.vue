<template>
  <div
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
</template>

<script setup>
import { Icon } from "@iconify/vue/dist/iconify.js";

const { project } = defineProps({
  project: {
    type: Object,
    required: true,
  },
});

const tagColors = {
  reactjs: "text-sky-500",
  vuejs: "text-mossGreen",
  nuxtjs: "text-mossGreen",
  gsap: "text-orangeGold",
  css: "text-orangeGold",
  tailwindcss: "text-orangeGold",
  typescript: "text-vermillion",
  javascript: "text-vermillion",
};
</script>

<style lang="scss" scoped></style>
