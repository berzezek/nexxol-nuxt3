<template>
  <nav class="bg-gray-800">
    <div class="container flex">
      <div class="px-8 py-4 bg-primary flex items-center cursor-pointer relative group">
                <span class="text-white">
                    <em class="fa-solid fa-bars"></em>
                </span>
        <span class="capitalize ml-2 text-white">Все категории</span>

        <div
            class="absolute w-full left-0 top-full bg-white shadow-md py-3 divide-y divide-gray-300 divide-dashed opacity-0 group-hover:opacity-100 transition duration-300 invisible group-hover:visible">
          <nuxt-link to="/" class="flex items-center px-6 py-3 hover:bg-gray-100 transition">
            <img src="/images/icons/sofa.svg" alt="sofa" class="w-5 h-5 object-contain">
            <span class="ml-6 text-gray-600 text-sm">Sofa</span>
          </nuxt-link>
          <nuxt-link href="#" class="flex items-center px-6 py-3 hover:bg-gray-100 transition">
            <img src="/images/icons/terrace.svg" alt="terrace" class="w-5 h-5 object-contain">
            <span class="ml-6 text-gray-600 text-sm">Terarce</span>
          </nuxt-link>
          <nuxt-link href="#" class="flex items-center px-6 py-3 hover:bg-gray-100 transition">
            <img src="/images/icons/bed.svg" alt="bed" class="w-5 h-5 object-contain">
            <span class="ml-6 text-gray-600 text-sm">Bed</span>
          </nuxt-link>
          <nuxt-link href="#" class="flex items-center px-6 py-3 hover:bg-gray-100 transition">
            <img src="/images/icons/office.svg" alt="office" class="w-5 h-5 object-contain">
            <span class="ml-6 text-gray-600 text-sm">office</span>
          </nuxt-link>
          <nuxt-link href="#" class="flex items-center px-6 py-3 hover:bg-gray-100 transition">
            <img src="/images/icons/outdoor-cafe.svg" alt="outdoor" class="w-5 h-5 object-contain">
            <span class="ml-6 text-gray-600 text-sm">Outdoor</span>
          </nuxt-link>
          <nuxt-link href="#" class="flex items-center px-6 py-3 hover:bg-gray-100 transition">
            <img src="/images/icons/bed-2.svg" alt="Mattress" class="w-5 h-5 object-contain">
            <span class="ml-6 text-gray-600 text-sm">Mattress</span>
          </nuxt-link>
        </div>
      </div>

      <div class="flex items-center justify-between flex-grow pl-12">
        <div class="flex items-center space-x-6 capitalize">
          <nuxt-link to="/" class="text-gray-200 hover:text-white transition">Home</nuxt-link>
          <nuxt-link to="/shop" class="text-gray-200 hover:text-white transition">Shop</nuxt-link>
          <nuxt-link to="#/about" class="text-gray-200 hover:text-white transition">About us</nuxt-link>
          <nuxt-link href="#/contacts" class="text-gray-200 hover:text-white transition">Contact us</nuxt-link>
        </div>
        <nuxt-link to="/login" class="text-gray-200 hover:text-white transition">Login</nuxt-link>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Nav"
}
</script>

<style scoped>

</style>