<script setup lang="ts">
import HomeView from '@/views/HomeView.vue'
import ExperienceView from '@/views/ExperienceView.vue'
import AboutMeView from '@/views/AboutMeView.vue'
import PortfolioView from './views/PortfolioView.vue'
import TitleComponent from './components/TitleComponent.vue'
import { MotionGroupComponent } from '@vueuse/motion'
</script>

<template>
  <div className="relative z-0 bg-primary">
    <div className="wrapper flex flex-col">
      <div id="hero" className="z-10">
        <HomeView />
      </div>
      <div class="relative z-30 bg-primary w-full pt-4">
        <MotionGroupComponent preset="slideVisibleOnceBottom" delay="200" duration="600">
          <TitleComponent title="About me" />
          <AboutMeView id="aboutMe" />
          <TitleComponent title="Portfolio" />
          <PortfolioView id="portfolio" />
          <TitleComponent title="Experience" />
          <ExperienceView id="experience" />
        </MotionGroupComponent>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
