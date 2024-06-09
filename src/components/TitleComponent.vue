<script setup lang="ts">
withDefaults(
  defineProps<{
    title?: string
  }>(),
  {
    title: ''
  }
)
</script>

<template>
  <div class="text-center mb-20 mt-6">
    <span class="text-white font-bold md:text-[80px] sm:text-[50px] text-[40px]">{{ title }}</span>
  </div>
</template>
