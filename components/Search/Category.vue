<template>
  <div class="flex items-center">
    <input type="checkbox" name="cat-1" id="cat-1"
           class="text-primary focus:ring-0 rounded-sm cursor-pointer">
    <label for="cat-1" class="text-gray-600 ml-3 cusror-pointer">{{ props.category.name }}</label>
<!--    <div class="ml-auto text-gray-600 text-sm">(кол-во)</div>-->
  </div>
</template>

<script setup>
const props = defineProps({
  category: {
    type: Object,
    required: true
  }
})

</script>

<style scoped>

</style>