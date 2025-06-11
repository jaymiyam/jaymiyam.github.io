<template>
  <Transition
    appear
    enter-from-class="opacity-0"
    leave-to-class="opacity-0"
    enter-active-class="transition ease-out duration-1000"
    leave-active-class="transition ease-in duration-1000"
    enter-to-class="opacity-100"
    leave-from-class="opacity-100"
  >
    <header
      class="flex w-full items-start justify-between py-6 sm:items-center"
    >
      <div>
        <span class="text-xl font-extrabold">jaymiyam.</span>
      </div>
      <nav>
        <ul class="flex flex-col items-end gap-2 sm:flex-row sm:gap-4">
          <li
            class="hover:text-mossGreen cursor-pointer font-bold transition hover:-translate-y-0.5"
          >
            <a
              class="flex gap-1"
              href="https://github.com/jaymiyam"
              target="_blank"
            >
              <span>github</span>
              <Icon icon="mingcute:github-line" width="24" height="24" />
            </a>
          </li>
          <li
            class="hover:text-mossGreen cursor-pointer font-bold transition hover:-translate-y-0.5"
          >
            <a
              class="flex gap-1"
              href="https://www.behance.net/jaymiyam"
              target="_blank"
            >
              <span>behance</span>
              <Icon icon="mingcute:behance-line" width="24" height="24" />
            </a>
          </li>
          <li
            class="hover:text-mossGreen cursor-pointer font-bold transition hover:-translate-y-0.5"
          >
            <a
              class="flex gap-1"
              href="https://www.linkedin.com/in/jaymi-yam/"
              target="_blank"
            >
              <span>linkedIn</span>
              <Icon icon="mingcute:linkedin-line" width="24" height="24" />
            </a>
          </li>
          <li
            class="hover:text-mossGreen cursor-pointer font-bold transition hover:-translate-y-0.5"
          >
            <a class="flex gap-1" href="mailto:jaymiyam@gmail.com">
              <span>email</span>
              <Icon icon="ic:outline-email" width="24" height="24" />
            </a>
          </li>
        </ul>
      </nav>
    </header>
  </Transition>
</template>

<script setup>
import { Icon } from "@iconify/vue/dist/iconify.js";
</script>
