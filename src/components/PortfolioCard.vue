<script lang="ts" setup>
const props = withDefaults(
  defineProps<{
    index: number
    image?: string
    name?: string
    description?: string
  }>(),
  { image: '', name: '', description: '' }
)

const isEven = props.index % 2 === 0
</script>

<template>
  <div
    :class="`w-full mt-[-2px] flex flex-col ${isEven ? 'lg:flex-row' : 'lg:flex-row-reverse'} gap-5`"
  >
    <div class="relative w-full lg:w-3/5">
      <img :src="image" alt="project_image" class="w-full h-auto object-cover rounded-3xl" />
    </div>

    <div
      :class="`w-full lg:w-2/5 px-6 md:p-16 flex flex-col justify-center ${isEven ? 'text-left lg:text-left' : 'text-left lg:text-right'}`"
    >
      <p
        class="text-white font-medium text-md sm:text-lg md:text-xl lg:text-2xl xl:text-3xl 2xl:text-4xl leading-tight"
      >
        {{ name }}
      </p>
      <p
        class="mt-4 text-secondary text-sm sm:text-xs md:text-sm lg:text-md xl:text-lg 2xl:text-xl"
      >
        {{ description }}
      </p>
    </div>
  </div>
</template>
