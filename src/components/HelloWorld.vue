<template>
  <div class="">
    <div class="w-full p-3 flex border-b md:px-20 lg:px-52 bg-white bg-opacity-50">
      <button @click="openWebPage('https://vercel.com/')" type="button" name="button">
        <img src="../assets/vercel.png" class="h-11" alt="">
      </button>
    </div>
    <div class="text-3xl uppercase font-extrabold p-12 text-center">
      Deploying a <span class="gradient-text blue">Vue,</span> <span class="gradient-text green">Vite,</span> and <span class="gradient-text purple">Tailwind</span> project to <span class="gradient-text orange">Vercel</span>
    </div>
    <div class="md:flex md:px-20 lg:px-52">
      <div class="md:w-1/2 p-4">
        <div class="bg-white p-6 shadow-xl rounded h-full">
          <p class="font-semibold text-2xl pb-4">Guide</p>
          <div class="p-4 rounded border overflow-auto h-80" style="background-color: #fafafa;">
            <BlogPost />
          </div>
          <button @click="openWebPage('https://vercel.com/blog/integrations-marketplace')" type="button" name="button" class="flex items-center pt-4 text-gray-500 hover:text-blue-500">
            <p class="text-sm mr-2">View Full Blog</p>
            <i class="fas fa-arrow-right text-xs"></i>
          </button>
        </div>
      </div>
      <!-- <div class="md:w-1/2 p-4">
        <div class="p-6 border rounded overflow-hidden h-full" style="background-color: #fafafa;">
          <p class="font-semibold text-2xl pb-4">Learn More</p>
          <div class="flex flex-wrap">
            <div v-for="item in cards" :key="item.name" class="md:w-1/2">
              <div class="px-2 py-4">
                <Card :name="item.name" :src="item.src" :logo="item.logo" :link="item.link"/>
              </div>
            </div>
          </div>
        </div>
      </div> -->
      <div class="md:w-1/2 p-4">
        <div class="p-6 border rounded overflow-hidden h-full" style="background-color: #fafafa;">
          <p class="font-semibold text-2xl pb-4">Learn More</p>
          <div class="flex flex-wrap">
            <div class="md:w-1/2">
              <div class="px-2 py-4">
                <div @click="openWebPage('https://vuejs.org/')" class="w-full h-full bg-white rounded-md shadow-md hover:shadow-lg">
                  <div class="relative w-full">
                    <img class="rounded-md" src="../assets/vueHome.png" alt="">
                  </div>
                  <div class="bg-white p-3 flex items-center">
                    <img src="../assets/logo.png" alt="" class="h-5 mr-2">
                    <p class="text-sm font-semibold text-gray-500 truncate"> Vue.js </p>
                  </div>
                </div>
              </div>
            </div>
            <div class="md:w-1/2">
              <div class="px-2 py-4">
                <div @click="openWebPage('https://tailwindcss.com/')" class="w-full h-full bg-white rounded-md shadow-md hover:shadow-lg">
                  <div class="relative w-full">
                    <img class="rounded-md" src="../assets/tailwindHome.png" alt="">
                  </div>
                  <div class="bg-white p-3 flex items-center">
                    <img src="../assets/tailwindcss.svg" alt="" class="h-5 mr-2">
                    <p class="text-sm font-semibold text-gray-500 truncate"> Tailwind CSS </p>
                  </div>
                </div>
              </div>
            </div>
            <div class="md:w-1/2">
              <div class="px-2 py-4">
                <div @click="openWebPage('https://vercel.com/')" class="w-full h-full bg-white rounded-md shadow-md hover:shadow-lg">
                  <div class="relative w-full">
                    <img class="rounded-md" src="../assets/vercelHome.png" alt="">
                  </div>
                  <div class="bg-white p-3 flex items-center">
                    <img src="../assets/vercelSmall.svg" alt="" class="h-5 mr-2">
                    <p class="text-sm font-semibold text-gray-500 truncate"> Vercel </p>
                  </div>
                </div>
              </div>
            </div>
            <div class="md:w-1/2">
              <div class="px-2 py-4">
                <div @click="openWebPage('https://vitejs.dev/')" class="w-full h-full bg-white rounded-md shadow-md hover:shadow-lg">
                  <div class="relative w-full">
                    <img class="rounded-md" src="../assets/viteHome.png" alt="">
                  </div>
                  <div class="bg-white p-3 flex items-center">
                    <img src="../assets/viteLogo.svg" alt="" class="h-5 mr-2">
                    <p class="text-sm font-semibold text-gray-500 truncate"> Vite </p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import BlogPost from './BlogPost.vue';
import Card from './Card.vue';
const cards = [
  {
    src: 'public/vueHome.png',
    logo: 'public/logo.png',
    name: 'Vue.js',
    link: 'https://vuejs.org/'
  },
  {
    src: 'public/tailwindHome.png',
    logo: 'public/tailwindcss.svg',
    name: 'Tailwind CSS',
    link: 'https://tailwindcss.com/'
  },
  {
    src: 'public/vercelHome.png',
    logo: 'public/vercelSmall.svg',
    name: 'Vercel',
    link: 'https://vercel.com/'
  },
  {
    src: 'public/viteHome.png',
    logo: 'public/viteLogo.svg',
    name: 'Vite',
    link: 'https://vitejs.dev/'
  },
]

export default {
  components: {
    BlogPost,
    Card
  },
  setup() {
    return {
      cards
    }
  },
  methods: {
    openWebPage(url) {
      window.open(url, "_blank");
    }
  },
}
</script>

<style media="screen">
.gradient-text {

/* Set the background size and repeat properties. */
background-size: 100%;
background-repeat: repeat;

/* Use the text as a mask for the background. */
/* This will show the gradient as a text color rather than element bg. */
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
-moz-background-clip: text;
-moz-text-fill-color: transparent;
}

.blue {
  /* Create the gradient. */
  background-image: linear-gradient(90deg, #3c80e7, #5ad4d8);
}

.green {
  /* Create the gradient. */
  background-image: linear-gradient(90deg, #58e061, #ffea4d);
}

.purple {
  /* Create the gradient. */
  background-image: linear-gradient(90deg, #762ebf, #dd3787);
}

.orange {
  /* Create the gradient. */
  background-image: linear-gradient(90deg, #ec6654, #f1bb50);
}

</style>
