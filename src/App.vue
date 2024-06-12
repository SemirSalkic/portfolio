<script setup lang="ts">
import HomeView from '@/views/HomeView.vue'
import ExperienceView from '@/views/ExperienceView.vue'
import AboutMeView from '@/views/AboutMeView.vue'
import PortfolioView from './views/PortfolioView.vue'
</script>

<template>
  <div className="relative z-0 bg-primary">
    <div className="wrapper flex flex-col">
      <div id="hero" className="z-10">
        <HomeView />
      </div>
      <div
        id="aboutMe"
        className="relative z-30 bg-primary w-full justify-center flex flex-col items-center"
      >
        <AboutMeView></AboutMeView>
      </div>
      <div id="portfolio" className="relative z-30 bg-primary w-full">
        <PortfolioView></PortfolioView>
      </div>
      <div id="experience" className="relative z-30 bg-primary w-full items-center flex flex-col">
        <ExperienceView />
      </div>
    </div>
  </div>
</template>

<style scoped></style>
