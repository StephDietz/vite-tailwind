<template>
  <div class="flex flex-col items-center justify-center">
    <img alt="Vercel logo" src="../assets/vercel.png" />
    <h1 class="text-7xl font-semibold text-white my-12">Develop. Preview. Ship.</h1>
    <div class="text-lg text-gray-300 text-center text-white">
      <p>Deployed by Vercel</p>
      <p>Built with Vue.js and Tailwind.css</p>
    </div>
    <div class="flex items-center mt-8">
      <img alt="Vue logo" class="h-10 mr-8" src="../assets/logo.png" />
      <img alt="Tailwind logo" class="h-8" src="../assets/tailwindcss.svg" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      count: 0
    }
  }
}
</script>
