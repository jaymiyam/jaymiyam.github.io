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
    <section>
      <h2 class="mb-10 text-3xl font-extrabold">playground</h2>
      <div class="grid gap-8 sm:grid-cols-2 sm:gap-12">
        <PlaygroundCard
          v-for="project in Playground"
          :key="project.id"
          :project="project"
        />
      </div>
    </section>
  </Transition>
</template>

<script setup>
import Playground from "../playground.json";
import PlaygroundCard from "./PlaygroundCard.vue";
</script>
