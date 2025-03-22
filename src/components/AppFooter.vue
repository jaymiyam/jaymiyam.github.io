<template>
  <Transition
    appear
    enter-from-class="opacity-0"
    leave-to-class="opacity-0"
    enter-active-class="transition ease-out duration-1000 delay-600"
    leave-active-class="transition ease-in duration-1000"
    enter-to-class="opacity-100"
    leave-from-class="opacity-100"
  >
    <footer
      class="grid items-center justify-between gap-4 border-t-2 border-t-stone-200 py-6 text-sm md:flex"
    >
      <div class="flex items-center gap-1">
        <Icon icon="line-md:email" width="24" height="24" />
        <span>jaymiyam@gmail.com</span>
      </div>
      <p>
        built with:
        <span class="text-orangeGold font-bold">JavaScript</span>,
        <span class="text-orangeGold font-bold">VueJS</span>,
        <span class="text-orangeGold font-bold">Tailwind</span>
      </p>
    </footer>
  </Transition>
</template>

<script setup>
import { Icon } from "@iconify/vue/dist/iconify.js";
</script>
