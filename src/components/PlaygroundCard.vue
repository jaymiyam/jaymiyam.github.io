<template>
  <div
    class="mb-8 flex flex-col gap-4 opacity-90 transition duration-300 hover:-translate-y-1.5 hover:opacity-100"
  >
    <div class="overflow-hidden rounded-md">
      <img
        :src="project.imagePath"
        alt="screenshot of mythology studio landing page"
      />
    </div>
    <div>
      <div class="mb-4 flex flex-col gap-2">
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
</script>

<style lang="scss" scoped></style>
