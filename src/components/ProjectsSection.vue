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
      <h2 class="mb-8 text-3xl font-extrabold">
        <button
          @click="showGraphicsProjects = false"
          :class="{ underline: !showGraphicsProjects }"
          class="hover:text-orangeGold cursor-pointer transition hover:-translate-y-0.5"
        >
          development
        </button>
        /
        <button
          @click="showGraphicsProjects = true"
          :class="{ underline: showGraphicsProjects }"
          class="hover:text-orangeGold cursor-pointer transition hover:-translate-y-0.5"
        >
          design
        </button>
      </h2>
      <div v-if="showGraphicsProjects">
        <div class="grid gap-8 sm:grid-cols-2 sm:gap-12">
          <!-- <GraphicsProjectCard
            v-for="project in GraphicsProjects"
            :key="project.id"
            :project="project"
            @click="openModal(project)"
          /> -->
          <WebflowProjectCard
            v-for="project in WebflowProjects"
            :key="project.id"
            :project="project"
          />
        </div>
        <p class="mb-8">
          Please check out my
          <a
            class="hover:text-orangeGold font-semibold underline transition"
            href="https://www.behance.net/jaymiyam"
            target="_blank"
            >Behance Portfolio</a
          >
          for more graphics work!
        </p>
      </div>
      <div v-else>
        <ProjectCard
          v-for="project in DevProjects"
          :key="project.id"
          :project="project"
        />
        <PlaygroundSection />
      </div>

      <ProjectModal
        v-if="selectedGraphicProject"
        :project="selectedGraphicProject"
        @close="selectedGraphicProject = null"
      />
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
