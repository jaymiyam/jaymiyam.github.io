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
          class="mb-4 text-4xl font-extrabold tracking-tight text-balance sm:mb-8 md:text-5xl"
        >
          Hi!I’m Jaymi, a creative developer.
        </h1>
        <p class="mb-8 text-balance">
          I design and code. This website is a curated collection of my
          projects.
        </p>
        <p class="text-balance">
          currently learning:
          <span class="text-orangeGold font-bold">D3.js</span>
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
