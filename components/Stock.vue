<template>
  <div class="container pb-16">
    <h2 class="text-2xl font-medium text-gray-800 uppercase mb-6">недавние поступления</h2>
    <div class="grid grid-cols-4 gap-6">
      <CardProduct
          v-for="product in stock"
          :key="product.id"
          :product="product"
      />
    </div>
  </div>
</template>

<script setup>
  const { data } = useFetch('http://localhost:8000/api/v1/product/')

  const stock = computed(() => {
    return data.value.result.slice(-4)
  })

</script>

<style scoped>

</style>