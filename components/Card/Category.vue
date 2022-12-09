<template>
  <div class="relative rounded-sm overflow-hidden group">
    <img :src="props.category.image" alt="category 1" class="w-full">
    <nuxt-link to="#"
       class="absolute inset-0 bg-black bg-opacity-40 flex items-center justify-center text-xl text-white font-roboto font-medium group-hover:bg-opacity-60 transition">{{ props.category.name }}</nuxt-link>
  </div>
</template>

<script setup>
  import { defineProps } from 'vue'
  const props = defineProps({
    category: {
      type: Object,
      required: true
    }
  })
</script>

<style scoped>

</style>