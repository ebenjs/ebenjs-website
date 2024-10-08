<script setup lang="ts">
import RoundedMiniCard from '@/components/RoundedMiniCard.vue'
import TechnoBadge from '@/components/TechnoBadge.vue'

const workingExperience = [
  {
    title: 'Senior Software Engineer',
    company: 'CGI Romania',
    companyLogo: 'cgi.png',
    date: 'Sep 2023 - Present'
  },
  {
    title: 'Software Engineer',
    company: 'Togolese Revenue Authority',
    companyLogo: 'otr.png',
    date: 'Mar 2021 - Sep 2023'
  },
  {
    title: 'Software Engineer',
    company: 'Worked remotely for Turing',
    companyLogo: 'turing.jpg',
    date: 'Mar 2022 - Aug 2022'
  },
  {
    title: 'Web Developer',
    company: 'Kaba Delivery',
    companyLogo: 'logo-blanc.svg',
    date: 'Jan 2018 - Apr 2019'
  }
]
</script>

<template>
  <main class="container mx-auto pt-12 px-4 sm:px-6 lg:px-8">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
      <div class="border-r md:border-r-0 md:pr-8 lg:border-r lg:pr-14">
        <p>
          <img
            src="@/assets/img/IMG_1514.jpg"
            alt="user"
            class="w-32 rounded-3xl mx-auto md:mx-0"
          />
        </p>
        <p class="custom-h1-title mt-8 text-center md:text-left">I'm Ebenezer Nikabou</p>
        <p class="mt-6 text-xl w-full md:w-2/3 text-center md:text-left mx-auto md:mx-0">
          Software Engineer, Web Developer, and Tech Enthusiast based in Bucharest, Romania. I love
          to build things that make life easier.
        </p>
        <div class="mt-5">
          <p class="custom-h3-title text-center md:text-left">
            I enjoy working with technologies like:
          </p>
          <div class="flex flex-wrap justify-center md:justify-start mt-10">
            <TechnoBadge src="angular-icon.svg" alt="angular" />
            <TechnoBadge src="spring.svg" alt="spring" class="ml-4" />
            <TechnoBadge src="vue-9.svg" alt="vuejs" class="ml-4" />
            <TechnoBadge src="symfony.svg" alt="symfony" class="ml-4" />
            <TechnoBadge src="mongodb-icon-2.svg" alt="mongodb" class="ml-4" />
          </div>
          <div class="flex flex-wrap justify-center md:justify-start mt-10">
            <TechnoBadge src="flutter-logo.svg" alt="flutter" />
            <TechnoBadge src="aws-2.svg" alt="AWS" class="ml-4" />
            <TechnoBadge src="nodejs-icon.svg" alt="nodeJS" class="ml-4" />
            <TechnoBadge src="docker.svg" alt="docker" class="ml-4" />
            <TechnoBadge src="postgresql.svg" alt="postgreSQL" class="ml-4" />
          </div>
        </div>
      </div>

      <div>
        <p class="custom-h1-title w-full md:w-4/5 text-center md:text-left">
          Passionate about building software solutions that solve real-world problems.
        </p>
        <div class="mt-8 flex justify-center md:justify-start">
          <button class="default-button">Talk with me</button>
          <button class="default-button-inversed ml-4">See my work</button>
          <button class="default-button-inversed ml-4 flex">
            <img src="@/assets/img/github-mark.png" alt="github" class="w-6" />
            <span class="ml-2">OpenSource</span>
          </button>
        </div>
        <section class="mt-14">
          <div class="divider"></div>
          <p class="custom-h3-title">Working Experience</p>
          <div class="pt-2">
            <RoundedMiniCard
              v-for="experience in workingExperience"
              :key="experience.title"
              :title="experience.title"
              :company="experience.company"
              :companyLogo="experience.companyLogo"
              :date="experience.date"
            />
          </div>
        </section>
      </div>
    </div>
  </main>
</template>
