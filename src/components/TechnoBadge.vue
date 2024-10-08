<script setup lang="ts">
defineProps({
  src: String,
  alt: String
})

const capitalizeFirstLetter = (word: string) => {
  return word.charAt(0).toUpperCase() + word.slice(1)
}
</script>

<template>
  <div class="flex flex-col bg-white">
    <div class="border border-b-0 pt-3 px-5 rounded-t-lg grow">
      <p class="w-14"><img :src="`/images/techno/${src}`" :alt="alt" /></p>
    </div>
    <p
      class="p-0 py-1 m-0 border border-t-0 rounded-b-lg bg-slate-100 text-sm font-semibold text-center"
    >
      {{ capitalizeFirstLetter(alt!) }}
    </p>
  </div>
</template>

<style scoped></style>
