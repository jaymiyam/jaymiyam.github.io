<template>
  <li
    class="hover:text-orangeGold flex items-center gap-2 transition hover:-translate-y-0.5"
  >
    <Icon :icon="icon" width="36" height="36" />
    <span class="font-bold">{{ text }}</span>
  </li>
</template>

<script setup>
import { Icon } from "@iconify/vue";
const { icon, text } = defineProps({
  icon: {
    type: String,
    required: true,
  },
  text: {
    type: String,
    required: true,
  },
});
</script>
