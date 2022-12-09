<template>
<div>


  <div class="container py-4 flex items-center gap-3">
    <nuxt-link href="/" class="text-primary text-base">
      <i class="fa-solid fa-house"></i>
    </nuxt-link>
    <span class="text-sm text-gray-400">
            <i class="fa-solid fa-chevron-right"></i>
        </span>
    <p class="text-gray-600 font-medium">Shop</p>
  </div>

  <div class="container grid grid-cols-4 gap-6 pt-4 pb-16 items-start">

    <div class="col-span-1 bg-white px-4 pb-6 shadow rounded overflow-hidden">
      <div class="divide-y divide-gray-200 space-y-5">
        <div>
          <h3 class="text-xl text-gray-800 mb-3 uppercase font-medium">Категории</h3>
          <div class="space-y-2">
            <SearchCategory
                v-for="category in categories"
                :key="category.id"
                :category="category"
            />
          </div>
        </div>

        <div class="pt-4">
          <h3 class="text-xl text-gray-800 mb-3 uppercase font-medium">Brands</h3>
          <div class="space-y-2">
            <div class="flex items-center">
              <input type="checkbox" name="brand-1" id="brand-1"
                     class="text-primary focus:ring-0 rounded-sm cursor-pointer">
              <label for="brand-1" class="text-gray-600 ml-3 cusror-pointer">Cooking Color</label>
              <div class="ml-auto text-gray-600 text-sm">(15)</div>
            </div>
            <div class="flex items-center">
              <input type="checkbox" name="brand-2" id="brand-2"
                     class="text-primary focus:ring-0 rounded-sm cursor-pointer">
              <label for="brand-2" class="text-gray-600 ml-3 cusror-pointer">Magniflex</label>
              <div class="ml-auto text-gray-600 text-sm">(9)</div>
            </div>
            <div class="flex items-center">
              <input type="checkbox" name="brand-3" id="brand-3"
                     class="text-primary focus:ring-0 rounded-sm cursor-pointer">
              <label for="brand-3" class="text-gray-600 ml-3 cusror-pointer">Ashley</label>
              <div class="ml-auto text-gray-600 text-sm">(21)</div>
            </div>
            <div class="flex items-center">
              <input type="checkbox" name="brand-4" id="brand-4"
                     class="text-primary focus:ring-0 rounded-sm cursor-pointer">
              <label for="brand-4" class="text-gray-600 ml-3 cusror-pointer">M&D</label>
              <div class="ml-auto text-gray-600 text-sm">(10)</div>
            </div>
            <div class="flex items-center">
              <input type="checkbox" name="brand-5" id="brand-5"
                     class="text-primary focus:ring-0 rounded-sm cursor-pointer">
              <label for="brand-5" class="text-gray-600 ml-3 cusror-pointer">Olympic</label>
              <div class="ml-auto text-gray-600 text-sm">(10)</div>
            </div>
          </div>
        </div>

        <div class="pt-4">
          <h3 class="text-xl text-gray-800 mb-3 uppercase font-medium">Цена</h3>
          <div class="mt-4 flex items-center">
            <input type="text" name="min" id="min"
                   class="w-full border-gray-300 focus:border-primary rounded focus:ring-0 px-3 py-1 text-gray-600 shadow-sm"
                   placeholder="мин">
            <span class="mx-3 text-gray-500">-</span>
            <input type="text" name="max" id="max"
                   class="w-full border-gray-300 focus:border-primary rounded focus:ring-0 px-3 py-1 text-gray-600 shadow-sm"
                   placeholder="макс">
          </div>
        </div>

        <div class="pt-4">
          <h3 class="text-xl text-gray-800 mb-3 uppercase font-medium">size</h3>
          <div class="flex items-center gap-2">
            <div class="size-selector">
              <input type="radio" name="size" id="size-xs" class="hidden">
              <label for="size-xs"
                     class="text-xs border border-gray-200 rounded-sm h-6 w-6 flex items-center justify-center cursor-pointer shadow-sm text-gray-600">XS</label>
            </div>
            <div class="size-selector">
              <input type="radio" name="size" id="size-sm" class="hidden">
              <label for="size-sm"
                     class="text-xs border border-gray-200 rounded-sm h-6 w-6 flex items-center justify-center cursor-pointer shadow-sm text-gray-600">S</label>
            </div>
            <div class="size-selector">
              <input type="radio" name="size" id="size-m" class="hidden">
              <label for="size-m"
                     class="text-xs border border-gray-200 rounded-sm h-6 w-6 flex items-center justify-center cursor-pointer shadow-sm text-gray-600">M</label>
            </div>
            <div class="size-selector">
              <input type="radio" name="size" id="size-l" class="hidden">
              <label for="size-l"
                     class="text-xs border border-gray-200 rounded-sm h-6 w-6 flex items-center justify-center cursor-pointer shadow-sm text-gray-600">L</label>
            </div>
            <div class="size-selector">
              <input type="radio" name="size" id="size-xl" class="hidden">
              <label for="size-xl"
                     class="text-xs border border-gray-200 rounded-sm h-6 w-6 flex items-center justify-center cursor-pointer shadow-sm text-gray-600">XL</label>
            </div>
          </div>
        </div>

        <div class="pt-4">
          <h3 class="text-xl text-gray-800 mb-3 uppercase font-medium">Color</h3>
          <div class="flex items-center gap-2">
            <div class="color-selector">
              <input type="radio" name="color" id="red" class="hidden">
              <label for="red"
                     class="border border-gray-200 rounded-sm h-6 w-6  cursor-pointer shadow-sm block"
                     style="background-color: #fc3d57;"></label>
            </div>
            <div class="color-selector">
              <input type="radio" name="color" id="black" class="hidden">
              <label for="black"
                     class="border border-gray-200 rounded-sm h-6 w-6  cursor-pointer shadow-sm block"
                     style="background-color: #000;"></label>
            </div>
            <div class="color-selector">
              <input type="radio" name="color" id="white" class="hidden">
              <label for="white"
                     class="border border-gray-200 rounded-sm h-6 w-6  cursor-pointer shadow-sm block"
                     style="background-color: #fff;"></label>
            </div>

          </div>
        </div>

      </div>
    </div>

    <div class="col-span-3">
      <div class="flex items-center mb-4">
        <div>
          <select name="sort" id="sort" v-model="sort"
                  class="border-gray-300 focus:border-primary rounded focus:ring-0 px-3 py-1 text-gray-600 shadow-sm">
            <option value="">По умолчанию</option>
            <option value="3">Цена: Низкая</option>
            <option value="4">Цена: Высокая</option>
            <option value="2">Сначала новые</option>
          </select>
        </div>
        <div class="flex gap-2 ml-auto">
          <div
              class="border border-primary w-10 h-9 flex items-center justify-center text-white bg-primary rounded cursor-pointer">
            <i class="fa-solid fa-grip-vertical"></i>
          </div>
          <div
              class="border border-gray-300 w-10 h-9 flex items-center justify-center text-gray-600 rounded cursor-pointer">
            <i class="fa-solid fa-list"></i>
          </div>
        </div>
      </div>

      <div class="grid grid-cols-3 gap-6">

        <CardProduct v-for="product in products.result" :key="product.id" :product="product" />

      </div>
    </div>
  </div>


</div>
</template>

<script setup lang="ts">
  const { data: products } = useFetch('http://localhost:8000/api/v1/product/')
  const { data: categories } = useFetch('http://localhost:8000/api/v1/category/')

  // get value from select form
  const sort = ref('')
  watch(sort, (value) => {
    if (value) {
      products.value.result.sort((a, b) => {
        if (value === '2') {
          return new Date(b.created_at) - new Date(a.created_at)
        }
        if (value === '3') {
          return a.price - b.price
        }
        if (value === '4') {
          return b.price - a.price
        }
      })
    }
  })
</script>

<style scoped>

</style>