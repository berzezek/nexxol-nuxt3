<template>
  <div class="container py-16">
    <h2 class="text-2xl font-medium text-gray-800 uppercase mb-6">категории товаров</h2>
    <div class="grid grid-cols-3 gap-3">
      <CardCategory
          v-for="category in data"
          :key="category.id"
          :category="category"
      />
    </div>
  </div>
</template>

<script setup>
  const { data } = useFetch('http://localhost:8000/api/v1/category/')

</script>

<style scoped>

</style>