<script setup lang="ts">
import HomeView from '@/views/HomeView.vue'
import ExperienceView from '@/views/ExperienceView.vue'
</script>

<template>
  <div className="relative z-0 bg-primary">
    <div className="wrapper">
      <div id="hero" className="z-10">
        <HomeView />
      </div>
      <div id="aboutMe" className="relative z-30 bg-primary mt-[-2px] w-full h-full">aaa</div>
      <div id="experience" className="relative z-30 bg-primary w-full"><ExperienceView /></div>
      <div id="contact" className="relative z-30 bg-primary w-full h-full">cccc</div>
    </div>
  </div>
</template>

<style scoped></style>
