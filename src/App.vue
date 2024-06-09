<script setup lang="ts">
import HomeView from '@/views/HomeView.vue'
import { ref } from 'vue'

const wrapperRef = ref(null)
</script>

<template>
  <div className="relative z-0 bg-primary">
    <div className="wrapper" ref="{wrapperRef}">
      <div id="hero" className="z-10">
        <HomeView scrollContainer="{wrapperRef}" />
      </div>
      <div id="portfolio" className="relative z-30 bg-primary mt-[-2px] w-full h-full">aaaaa</div>
      <div id="experience" className="relative z-30 bg-primary w-full h-full">bbbb</div>
      <div id="contact" className="relative z-30 bg-primary w-full h-full">cccc</div>
    </div>
  </div>
</template>

<style scoped></style>
