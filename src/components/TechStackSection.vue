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
          <h3 class="mb-4">webdev</h3>
          <ul class="grid grid-flow-row gap-2">
            <TechStackItem icon="skill-icons:html" text="HTML5" />
            <TechStackItem icon="skill-icons:css" text="CSS" />
            <TechStackItem icon="skill-icons:javascript" text="JavaScript" />
            <TechStackItem icon="skill-icons:git" text="Git" />
          </ul>
        </div>
        <div>
          <h3 class="mb-4">frameworks</h3>
          <ul class="grid grid-flow-row gap-2">
            <TechStackItem icon="material-icon-theme:react" text="React" />
            <TechStackItem icon="devicon:vuejs" text="VueJS" />
            <TechStackItem icon="devicon:tailwindcss" text="TailwindCSS" />
            <TechStackItem icon="logos:greensock-icon" text="GSAP" />
          </ul>
        </div>
        <div>
          <h3 class="mb-4">design</h3>
          <ul class="grid grid-flow-row gap-2">
            <TechStackItem icon="skill-icons:webflow" text="Webflow" />
            <TechStackItem icon="devicon:figma" text="Adobe Figma" />
            <TechStackItem icon="devicon:illustrator" text="Adobe Illusrator" />
            <TechStackItem icon="devicon:photoshop" text="Adobe Photoshop" />
          </ul>
        </div>
      </div>
    </section>
  </Transition>
</template>

<script setup>
import TechStackItem from "./TechStackItem.vue";
</script>
