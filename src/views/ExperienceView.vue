<script setup lang="ts">
import { ref } from 'vue'
import { TabGroup, TabList, Tab, TabPanels, TabPanel } from '@headlessui/vue'
import TitleComponent from '@/components/TitleComponent.vue'

const experience = ref([
  {
    id: 1,
    jobTitle: 'Frontend developer',
    company: 'vAudience GmbH',
    location: 'Wurzburg, Germany',
    date: '14/08/2020 - 24/11/2023',
    details: [
      'Develop highly interactive user interfaces using Vue.js (Versions 2 & 3), integrating TypeScript for type safety and scalability',
      'Implement responsive layouts with Tailwind CSS or Vuetify, and managed application state using Vuex and Pinia for Vue 2 and Vue 3, respectively.',
      'Enhanced user experience by implementing a Chat component with Admin Panel functionalities.',
      'Used Axios to fetch data from the server.',
      'Implemented Storybook to build and test UI components in isolation, ensuring consistency across the application.',
      'Implemented Cypress for end-to-end testing across the whole application.',
      'Mentored and guided junior developers to help them improve and push the team towards an always learning culture.',
      'Developed Mobile Applications with Flutter, employing the Bloc pattern for maintainable and predictable state management.',
      'Collaborated with cross-functional teams, utilizing tools like GitHub, ClickUp, Slack, Swagger, Jira, Confluence, Trello, and Insomnia for project tracking and documentation.'
    ]
  },
  {
    id: 2,
    jobTitle: 'Programmer',
    company: 'SELECT D.O.O.',
    location: 'Tuzla, Bosnia and Herzegovina',
    date: '31/7/2019 - 31/7/2020',
    details: [
      'Developed and maintained Windows platform applications, focusing on design and functionality.',
      'Specialized in creating Enterprise Resource Planning (ERP) systems, streamlining business processes and enhancing operational efficiency.',
      'Crafted modern and responsive websites using HTML and WordPress.',
      'Proficient in WPF C# and XAML, delivering high-performance applications with intuitive user interfaces.'
    ]
  }
])
</script>

<template>
  <div class="w-full py-16 px-4">
    <TitleComponent title="Experience" />
    <TabGroup>
      <div class="flex items-center h-full justify-center">
        <TabList class="flex flex-col w-3/4 rounded-xl p-1 mr-1">
          <Tab
            v-for="exp in experience"
            as="template"
            :key="exp.id"
            v-slot="{ selected }"
            class="my-1"
          >
            <button
              :class="[
                'w-full rounded-lg py-2.5 text-sm font-medium leading-5',
                'ring-white/60 ring-offset-2 ring-offset-quaternary focus:outline-none focus:ring-2',
                selected
                  ? 'bg-white text-tertiary shadow'
                  : 'text-blue-100 hover:bg-white/[0.12] hover:text-white'
              ]"
            >
              <div class="flex flex-col items-center">
                <span class="text-lg font-semibold">{{ exp.jobTitle }}</span>
                <span class="font-semibold">{{ exp.company }}</span>
                <span class="font-semibold">{{ exp.location }}</span>
                <span class="font-semibold">{{ exp.date }}</span>
              </div>
            </button>
          </Tab>
        </TabList>

        <TabPanels class="mt-2 w-full ml-1 space-y-4">
          <TabPanel
            v-for="(exp, idx) in experience"
            :key="idx"
            class="rounded-xl border-4 p-3 focus:outline-none shadow-lg bg-gradient-to-r from-primary to-tertiary text-white"
          >
            <div class="flex flex-col space-y-2">
              <div class="flex justify-between items-center">
                <span class="text-lg font-bold">{{ exp.jobTitle }}</span>
                <span class="font-medium">{{ exp.date }}</span>
              </div>
              <ul class="list-disc list-inside pl-5 space-y-1">
                <li v-for="(detail, idx) in exp.details" :key="idx" class="font-medium">
                  {{ detail }}
                </li>
              </ul>
            </div>
          </TabPanel>
        </TabPanels>
      </div>
    </TabGroup>
  </div>
</template>
