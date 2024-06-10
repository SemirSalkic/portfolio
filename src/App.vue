<script setup lang="ts">
import HomeView from '@/views/HomeView.vue'
import ExperienceView from '@/views/ExperienceView.vue'
import AboutMeView from '@/views/AboutMeView.vue'
</script>

<template>
  <div className="relative z-0 bg-primary">
    <div className="wrapper">
      <div id="hero" className="z-10">
        <HomeView />
      </div>
      <div
        id="aboutMe"
        className="relative z-30 bg-primary w-full justify-center flex flex-col items-center"
      >
        <AboutMeView></AboutMeView>
      </div>
      <div id="experience" className="relative z-30 bg-primary w-full items-center flex flex-col">
        <ExperienceView />
      </div>
      <div id="contact" className="relative z-30 bg-primary w-full h-full">cccc</div>
    </div>
  </div>
</template>

<style scoped></style>
