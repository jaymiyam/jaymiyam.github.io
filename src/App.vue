<template>
  <div class="mx-8 md:w-[760px] lg:w-[800px]">
    <AppHeader />
    <main>
      <AboutSection />
      <TechStackSection />
      <ProjectsSection />
    </main>
    <AppFooter />
  </div>
</template>

<script setup>
import AppHeader from "./components/AppHeader.vue";
import AboutSection from "./components/AboutSection.vue";
import TechStackSection from "./components/TechStackSection.vue";
import ProjectsSection from "./components/ProjectsSection.vue";
import AppFooter from "./components/AppFooter.vue";
</script>
