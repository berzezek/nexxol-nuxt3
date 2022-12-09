<template>
  <div class="container pb-16">
    <h2 class="text-2xl font-medium text-gray-800 uppercase mb-6">рекомендуем товары для вас</h2>
    <div class="grid grid-cols-4 gap-6">
      <CardProduct
          v-for="product in recomended"
          :key="product.id"
          :product="product"
      />
    </div>
  </div>
</template>

<script setup>
const { data } = useFetch('http://localhost:8000/api/v1/product/')

const recomended = computed(() => {
  // randomize array and slice 8 elements
  return data.value.result.sort(() => Math.random() - 0.5).slice(0, 8)
})

</script>

<style scoped>

</style>