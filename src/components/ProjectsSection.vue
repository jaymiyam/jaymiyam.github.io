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
        <ProjectCard
          v-for="project in Projects"
          :key="project.id"
          :project="project"
        />
      </div>
    </section>
  </Transition>
</template>

<script setup>
import Projects from "../projects.json";
import ProjectCard from "./ProjectCard.vue";
</script>
