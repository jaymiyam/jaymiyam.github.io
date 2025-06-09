<template>
  <Transition
    appear
    enter-from-class="opacity-0"
    leave-to-class="opacity-0"
    enter-active-class="transition ease-out duration-200"
    leave-active-class="transition ease-in duration-200"
    enter-to-class="opacity-100"
    leave-from-class="opacity-100"
  >
    <div
      class="fixed inset-0 z-99 flex items-center justify-center bg-black/75 p-4"
    >
      <div class="relative h-full w-full max-w-3xl rounded-lg bg-white p-10">
        <!-- Close Button -->
        <button
          @click="emitClose"
          class="hover:text-orangeGold absolute top-4 right-4 cursor-pointer text-3xl text-black"
        >
          &times;
        </button>
        <!-- Image Carousel -->
        <div class="h-full space-y-4 overflow-y-auto whitespace-nowrap">
          <img
            v-for="(img, i) in project.galleryImages"
            :key="i"
            :src="img"
            alt=""
            class="mx-auto block max-h-full w-auto rounded shadow"
          />
        </div>
      </div>
    </div>
  </Transition>
</template>

<script setup>
import { onMounted, onUnmounted } from "vue";

const { project } = defineProps({
  project: {
    type: Object,
    required: true,
  },
});
const emit = defineEmits(["close"]);

onMounted(() => {
  window.addEventListener("keydown", onEsc);
});

onUnmounted(() => {
  window.removeEventListener("keydown", onEsc);
});

function emitClose() {
  emit("close");
}

function onEsc(e) {
  if (e.key === "Escape") emitClose();
}
</script>
