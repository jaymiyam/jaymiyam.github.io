<template>
  <div
    class="mb-12 flex flex-col gap-4 opacity-90 transition duration-300 hover:-translate-y-1.5 hover:opacity-100"
  >
    <div class="overflow-hidden rounded-md">
      <a :href="project.demoLink" target="_blank">
        <img
          :src="project.imagePath"
          alt="screenshot of mythology studio landing page"
        />
      </a>
    </div>
    <div>
      <a :href="project.demoLink" target="_blank">
        <h3 class="mb-4 text-2xl font-extrabold underline">
          {{ project.name }}
        </h3>
      </a>
      <p>
        {{ project.description }}
      </p>
    </div>
  </div>
</template>

<script setup>
const { project } = defineProps({
  project: {
    type: Object,
    required: true,
  },
});
</script>
