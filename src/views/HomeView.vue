<script setup lang="ts">
import SpacemanAnimation from '@/components/AstronautModel.vue'
</script>

<template>
  <main>
    <div>
      <section className="parallax">
        <div
          className="parallax__content absolute top-[10%] sm:top-[16%] lg:top-[24%] w-full mx-auto lg:pl-[38vh] lg:pr-[30vh] xl:pl-96 xl:pr-72 2xl:px-40 3xl:px-60 flex flex-col lg:flex-row items-start z-10"
        >
          <div className="flex-1 lg:mb-0">
            <h1
              className="font-medium text-white text-[40px] xs:text-[50px] sm:text-[68px] md:text-[80px] lg:text-[100px] 2xl:text-[180px] leading-[110px] 2xl:leading-[160px]"
            >
              SALKIĆ SEMIR
            </h1>
          </div>
          <div
            className="flex-1 flex justify-start lg:justify-end mt-4 sm:mt-14 ml-8 xs:ml-[-4vh] sm:ml-[-17vh] md:ml-[-26vh] lg:mt-10 2xl:mt-0"
          >
            <div
              className="font-bold text-[20px] sm:text-[30px] md:text-[36px] 2xl:text-[46px] sm:leading-[40px] md:leading-[50px] 2xl:leading-[60px] streaky-glow max-w-sm 2xl:max-w-lg text-white text-left"
            >
              Crafting pixels into experiences, <br />
              one line of code at a time.
            </div>
          </div>
        </div>

        <img className="parallax__stars" src="../assets/parallax/1Stars.svg" alt="" />
        <img className="parallax__planets" src="../assets/parallax/2Planets.svg" alt="" />
        <img className="parallax__mountain1" src="../assets/parallax/3Mountain.svg" alt="" />
        <img className="parallax__mountain2" src="../assets/parallax/4Mountain.svg" alt="" />
        <img className="parallax__crater" src="../assets/parallax/5Crater.svg" alt="" />
        <img className="parallax__sun" src="../assets/parallax/6Sun.svg" alt="" />

        <div class="relative z-10">
          <SpacemanAnimation class="absolute inset-0" />
          <div class="absolute inset-0 bg-black bg-opacity-0 z-20"></div>
        </div>
      </section>
    </div>
  </main>
</template>
