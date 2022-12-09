<template>
  <div class="container py-16">
    <div class="w-10/12 grid grid-cols-3 gap-6 mx-auto justify-center">
      <div class="border border-primary rounded-sm px-3 py-6 flex justify-center items-center gap-5">
        <img src="/images/icons/delivery-van.svg" alt="Delivery" class="w-12 h-12 object-contain">
        <div>
          <h4 class="font-medium capitalize text-lg">Служба доставки</h4>
          <p class="text-gray-500 text-sm">Order over $200</p>
        </div>
      </div>
      <div class="border border-primary rounded-sm px-3 py-6 flex justify-center items-center gap-5">
        <img src="/images/icons/money-back.svg" alt="Delivery" class="w-12 h-12 object-contain">
        <div>
          <h4 class="font-medium capitalize text-lg">Экономия средств</h4>
          <p class="text-gray-500 text-sm">30 days money returs</p>
        </div>
      </div>
      <div class="border border-primary rounded-sm px-3 py-6 flex justify-center items-center gap-5">
        <img src="/images/icons/service-hours.svg" alt="Delivery" class="w-12 h-12 object-contain">
        <div>
          <h4 class="font-medium capitalize text-lg">Поддержка 24/7</h4>
          <p class="text-gray-500 text-sm">Customer support</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Benefits"
}
</script>

<style scoped>

</style>