<script setup lang="ts">
import TitleComponent from '@/components/TitleComponent.vue'
</script>

<template>
  <div class="flex items-center flex-col">
    <TitleComponent title="About me"></TitleComponent>
    <div class="flex flex-wrap items-center justify-center">
      <div class="text-white px-10 w-full md:w-1/2">
        <div
          class="rounded-xl border-4 p-3 focus:outline-none shadow-lg bg-gradient-to-r from-primary to-tertiary text-white"
        >
          <p class="text-lg mb-2">
            My name is Semir Salkić and I am a Frontend Developer. I was born on January 19, 1998 in
            Bosnia and Herzegovina. I hold a Bachelor of Engineering Informatics degree from
            EMPIRICA College of Computing and Business Communications in Tuzla, Bosnia and
            Herzegovina.
          </p>
          <p class="text-lg mb-2">
            I have extensive experience in frontend development, particularly in working with Vue.js
            and TypeScript. I am also proficient in responsive web design and complex application
            development, utilizing frameworks like Tailwind CSS, Vuetify, CSS, and SCSS.
          </p>
          <p class="text-lg mb-2">
            Throughout my career, I have gained hands-on experience in building real-time chat
            applications with admin panel functionalities, as well as developing cross-platform
            mobile applications using Flutter. I am familiar with UI component development and
            testing, and I have a strong understanding of version control and project management
            tools.
          </p>
          <p class="text-lg mb-2">
            In addition to my technical skills, I have honed my organizational and communication
            abilities. I am adept at managing multiple projects simultaneously, ensuring timely
            completion and adherence to quality standards. I have experience leading and mentoring
            teams, fostering a collaborative environment that encourages innovation and
            productivity.
          </p>
          <p class="text-lg">
            I am excited to continue growing as a frontend developer and contributing my skills to
            innovative projects. I am committed to continuous improvement, regularly evaluating and
            refining workflows to enhance team performance.
          </p>
        </div>
      </div>
      <img class="w-full md:w-1/3 h-auto" src="../assets/picture1.png" alt="student" />
    </div>
  </div>
</template>
