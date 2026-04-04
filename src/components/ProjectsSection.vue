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
          v-for="project in DevProjects"
          :key="project.id"
          :project="project"
        />
        <PlaygroundSection />
      </div>
    </section>
  </Transition>
</template>

<script setup>
import { ref } from "vue";
import PlaygroundSection from "./PlaygroundSection.vue";
import DevProjects from "../developmentProjects.json";
import ProjectCard from "./ProjectCard.vue";
import WebflowProjects from "../webflowProjects.json";
import WebflowProjectCard from "./WebflowProjectCard.vue";
// import GraphicsProjects from "../graphicsProjects.json";
// import GraphicsProjectCard from "./GraphicsProjectCard.vue";
// import ProjectModal from "./ProjectModal.vue";

const showGraphicsProjects = ref(false);
// const selectedGraphicProject = ref(null);

// function openModal(project) {
//   selectedGraphicProject.value = project;
// }
</script>
