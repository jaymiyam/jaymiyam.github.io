<template>
  <Transition
    appear
    enter-from-class="opacity-0"
    leave-to-class="opacity-0"
    enter-active-class="transition ease-out duration-1000 delay-150"
    leave-active-class="transition ease-in duration-1000"
    enter-to-class="opacity-100"
    leave-from-class="opacity-100"
  >
    <section
      class="flex flex-col-reverse gap-8 pt-10 sm:grid sm:grid-cols-2 sm:pt-20"
    >
      <div>
        <h1
          class="mb-4 text-4xl font-extrabold tracking-tight sm:mb-8 md:text-5xl"
        >
          Hi!I’m Jaymi, a front-end developer.
        </h1>
        <p class="mb-8">
          this website is a curated collection of my web design and development
          projects.
        </p>
        <p>
          currently learning:
          <span class="text-orangeGold font-bold">TypeScript</span>,
          <span class="text-orangeGold font-bold">React</span>
        </p>
      </div>
      <div>
        <Vue3Lottie :animationData="CatJSON" />
      </div>
    </section>
  </Transition>
</template>

<script setup>
import { Vue3Lottie } from "vue3-lottie";
import CatJSON from "../assets/designer_cat_crop2.json";
</script>
