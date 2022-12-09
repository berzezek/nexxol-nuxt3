<template>
  <div class="bg-white shadow rounded overflow-hidden group">
    <div class="relative">
      <img :src="props.product.get_thumbnail" :alt="props.product.name" class="w-full">
      <div class="absolute inset-0 bg-black bg-opacity-40 flex items-center
                    justify-center gap-2 opacity-0 group-hover:opacity-100 transition">

      </div>
    </div>
    <div class="pt-4 pb-3 px-4">
      <a href="#">
        <h4 class="uppercase font-medium text-xl mb-2 text-gray-800 hover:text-primary transition">
          {{ props.product.name}}</h4>
      </a>
      <div class="flex items-baseline mb-1 space-x-2">
        <p class="text-xl text-primary font-semibold">{{ priceByDigits(props.product.price) }}</p>
        <p class="text-sm text-gray-400 line-through">$55.90</p>
      </div>
      <div class="flex items-center">
        <div class="flex gap-1 text-sm text-yellow-400">
          <span><em class="fa-solid fa-star"></em></span>
          <span><em class="fa-solid fa-star"></em></span>
          <span><em class="fa-solid fa-star"></em></span>
          <span><em class="fa-solid fa-star"></em></span>
          <span><em class="fa-solid fa-star"></em></span>
        </div>
        <div class="text-xs text-gray-500 ml-3">(150)</div>
      </div>
    </div>
    <nuxt-link to="#"
       class="block w-full py-1 text-center text-white bg-primary border border-primary rounded-b hover:bg-transparent hover:text-primary transition">Подробнее</nuxt-link>
  </div>
</template>

<script setup>
  import { defineProps } from 'vue'
  const props = defineProps({
    product: {
      type: Object,
      required: true
    }
  })

  const priceByDigits = (price) => {
    return price.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ' ')
  }

</script>

<style scoped>

</style>