<template>
  <div
    class="mb-12 flex cursor-pointer flex-col gap-4 opacity-90 transition duration-300 hover:-translate-y-1.5 hover:opacity-100"
  >
    <div class="overflow-hidden rounded-md">
      <img
        :src="project.imagePath"
        alt="screenshot of mythology studio landing page"
      />
    </div>
    <div>
      <h3 class="mb-4 text-2xl font-extrabold">{{ project.name }}</h3>
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
