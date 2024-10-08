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
    title: 'Web Developer',
    company: 'Company B',
    companyLogo: '@/assets/img/companies/company-b-logo.png',
    date: '2017 - 2019'
  }
]
</script>

<template>
  <main class="container mx-auto pt-12">
    <div class="grid grid-cols-2">
      <div class="border-r">
        <p>
          <img src="@/assets/img/IMG_1514.jpg" alt="user" class="w-32 rounded-3xl" />
        </p>
        <p class="custom-h1-title mt-8">I'm Ebenezer Nikabou</p>
        <p class="mt-6 text-xl w-2/3">
          Software Engineer, Web Developer, and Tech Enthusiast based in Bucharest, Romania. I love
          to build things that make life easier.
        </p>
        <div class="mt-5">
          <p class="custom-h3-title">I enjoy working with technologies like:</p>
          <div class="flex mt-10">
            <TechnoBadge src="angular-icon.svg" alt="angular" />
            <TechnoBadge src="spring.svg" alt="spring" class="ml-10" />
            <TechnoBadge src="vue-9.svg" alt="vuejs" class="ml-10" />
            <TechnoBadge src="symfony.svg" alt="symfony" class="ml-10" />
            <TechnoBadge src="mongodb-icon-2.svg" alt="mongodb" class="ml-10" />
          </div>
          <div class="flex mt-10">
            <TechnoBadge src="flutter-logo.svg" alt="flutter" />
            <TechnoBadge src="aws-2.svg" alt="AWS" class="ml-10" />
            <TechnoBadge src="nodejs-icon.svg" alt="nodeJS" class="ml-10" />
            <TechnoBadge src="docker.svg" alt="docker" class="ml-10" />
            <TechnoBadge src="postgresql.svg" alt="postgreSQL" class="ml-10" />
          </div>
        </div>
      </div>
      <!-- ... -->
      <div class="pl-14">
        <p class="custom-h1-title w-4/5">
          Passionate about building software solutions that solve real-world problems.
        </p>
        <div class="mt-8 flex">
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
