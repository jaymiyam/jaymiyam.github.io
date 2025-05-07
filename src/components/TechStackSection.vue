<template>
  <Transition
    appear
    enter-from-class="opacity-0"
    leave-to-class="opacity-0"
    enter-active-class="transition ease-out duration-1000 delay-300"
    leave-active-class="transition ease-in duration-1000"
    enter-to-class="opacity-100"
    leave-from-class="opacity-100"
  >
    <section class="pt-20">
      <h2 class="mb-8 text-3xl font-extrabold">techStack</h2>
      <div class="grid grid-cols-2 gap-x-2 gap-y-8 sm:grid-cols-3 sm:gap-y-0">
        <div>
          <h3 class="mb-4">languages</h3>
          <ul class="grid grid-flow-row gap-2">
            <li
              class="hover:text-orangeGold flex items-center gap-2 transition hover:-translate-y-0.5"
            >
              <Icon icon="skill-icons:html" width="36" height="36" />
              <span class="font-bold">HTML5</span>
            </li>
            <li
              class="hover:text-orangeGold flex items-center gap-2 transition hover:-translate-y-0.5"
            >
              <Icon icon="skill-icons:css" width="36" height="36" />
              <span class="font-bold">CSS3</span>
            </li>
            <li
              class="hover:text-orangeGold flex items-center gap-2 transition hover:-translate-y-0.5"
            >
              <Icon icon="skill-icons:javascript" width="36" height="36" />
              <span class="font-bold">JavaSript</span>
            </li>
          </ul>
        </div>
        <div>
          <h3 class="mb-4">frameworks</h3>
          <ul class="grid grid-flow-row gap-2">
            <li
              class="hover:text-orangeGold flex items-center gap-2 transition hover:-translate-y-0.5"
            >
              <Icon icon="devicon:vuejs" width="36" height="36" />
              <span class="font-bold">VueJS</span>
            </li>
            <li
              class="hover:text-orangeGold flex items-center gap-2 transition hover:-translate-y-0.5"
            >
              <Icon icon="material-icon-theme:nuxt" width="36" height="36" />
              <span class="font-bold">NuxtJS</span>
            </li>
            <li
              class="hover:text-orangeGold flex items-center gap-2 transition hover:-translate-y-0.5"
            >
              <Icon icon="material-icon-theme:react" width="36" height="36" />
              <span class="font-bold">React</span>
            </li>
            <li
              class="hover:text-orangeGold flex items-center gap-2 transition hover:-translate-y-0.5"
            >
              <Icon icon="devicon:tailwindcss" width="36" height="36" />
              <span class="font-bold">TailwindCSS</span>
            </li>
          </ul>
        </div>
        <div>
          <h3 class="mb-4">utilities</h3>
          <ul class="grid grid-flow-row gap-2">
            <li
              class="hover:text-orangeGold flex items-center gap-2 transition hover:-translate-y-0.5"
            >
              <Icon icon="skill-icons:git" width="36" height="36" />
              <span class="font-bold">Git</span>
            </li>
            <li
              class="hover:text-orangeGold flex items-center gap-2 transition hover:-translate-y-0.5"
            >
              <Icon icon="devicon:github" width="36" height="36" />
              <span class="font-bold">GitHub</span>
            </li>
            <li
              class="hover:text-orangeGold flex items-center gap-2 transition hover:-translate-y-0.5"
            >
              <Icon icon="devicon:vitest" width="36" height="36" />
              <span class="font-bold">Vitest</span>
            </li>
            <li
              class="hover:text-orangeGold flex items-center gap-2 transition hover:-translate-y-0.5"
            >
              <Icon icon="logos:greensock-icon" width="36" height="36" />
              <span class="font-bold">GSAP</span>
            </li>
          </ul>
        </div>
      </div>
    </section>
  </Transition>
</template>

<script setup>
import { Icon } from "@iconify/vue/dist/iconify.js";
</script>
