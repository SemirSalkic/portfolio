<script setup lang="ts">
import PortfolioCard from '@/components/PortfolioCard.vue'
import SED from '@/assets/projects/SED.png'
import SEW from '@/assets/projects/SEW.png'
import WA from '@/assets/projects/WA.gif'

const portfolio = [
  {
    id: 1,
    name: 'ShortEats: Culinary Quick Clips - Secure Login Portal',
    description:
      'Welcome to “ShortEats,” where flavor meets brevity. Our secure login portal is your gateway to a world of culinary delights, captured in quick, engaging video clips. Designed with food enthusiasts in mind, this authentication page is the first step to discovering and sharing bite-sized cooking inspirations. With a user-friendly interface, robust security, and a dash of aesthetic appeal, logging in is just as pleasant as watching our delectable food shorts.',
    image: SEW
  },
  {
    id: 2,
    name: 'ShortEats: Gourmet Snippets - Dark Mode Authentication',
    description:
      'Dive into the night kitchen with “ShortEats: Gourmet Snippets,” featuring our dark mode authentication interface. This sleek and sophisticated login page is designed for those who prefer culinary exploration after dusk. The contrasting white-on-black elements highlight the ease of navigation, ensuring a smooth entry into a realm of quick, flavorful video recipes. Embrace the elegance of dark mode as you sign in to share or discover the latest in food videography.',
    image: SED
  },
  {
    id: 3,
    name: 'Weather Application: Your Personal Meteorologist',
    description:
      'Embark on a meteorological journey with our “Weather Application,” your personal guide to the skies. This application offers a user-friendly platform to keep track of the weather conditions in your favorite cities. With features like an autocomplete search bar, current weather data display, and a 5-day forecast, planning your days has never been easier. Add cities to your favorites for quick access, and remove them just as easily. Our responsive design ensures a seamless experience on both mobile and desktop devices, with a clean and intuitive UI that makes weather tracking a breeze.',
    image: WA
  }
]
</script>

<template>
  <div class="px-10 flex flex-col gap-10 md:gap-20">
    <div v-for="item in portfolio" :key="item.id">
      <PortfolioCard
        :index="item.id"
        :name="item.name"
        :description="item.description"
        :image="item.image"
      />
    </div>
  </div>
</template>
