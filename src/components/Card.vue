<template>
  <div @click="openWebPage(link)" class="w-full h-full bg-white rounded-md shadow-md hover:shadow-lg">
    <div class="relative w-full">
      <img class="rounded-md" :src="src" alt="">
      <!-- <div class="bg-white bg-opacity-75 absolute inset-0 flex items-center justify-center">
        <i class="fas fa-arrow-alt-circle-right text-4xl text-gray-800"></i>
      </div> -->
    </div>
    <div class="bg-white p-3 flex items-center">
      <img :src="logo" alt="" class="h-5 mr-2">
      <p class="text-sm font-semibold text-gray-500 truncate"> {{name}} </p>
    </div>
  </div>
</template>

<script>
//import tailwindHome.png from './tailwindHome.png';
export default {
  props: ['src', 'logo', 'name', 'link'],
  methods: {
    openWebPage(url) {
      window.open(url, "_blank");
    }
  },
}
</script>

<style lang="css" scoped>
</style>
