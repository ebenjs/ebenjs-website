<script setup lang="ts">
defineProps({
  title: String,
  company: String,
  companyLogo: String,
  date: String
})
</script>

<template>
  <div>
    <div class="rounded-mini-card">
      <div class="flex items-center">
        <img :src="`/images/companies/${companyLogo}`" alt="company" class="w-16 rounded-full" />
        <div class="ml-4 grow">
          <div class="flex flex-col">
            <p class="custom-h3-title">
              {{ title }}
            </p>
            <p>{{ company }}</p>
          </div>
        </div>
        <p class="text-sm">
          {{ date }}
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.rounded-mini-card {
  margin-top: 1.5rem;
}
</style>
