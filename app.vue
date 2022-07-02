<script setup lang="ts">
const showStartModal = ref(false)

const windowSize = {
  height: window.innerHeight,
  width: window.innerWidth
}
</script>

<template>
  <svg class="absolute" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
    <line x1="0" y1="80" x2="100" y2="20" stroke="white" />

    <!-- If you do not specify the stroke
       color the line will not be visible -->
  </svg>
  <div class="relative">

    <div class="absolute grid grid-cols-2 grid-rows-2 main-wrapper cursor-pointer">
      <div>1</div>
      <div>1</div>
      <div>1</div>
      <div>1</div>
    </div>
  </div>


  <div v-show="showStartModal" class="relative flex justify-center items-center">
    <div class="w-full h-full bg-white bg-opacity-30 top-0 fixed sticky-0 px-2 py-2">

      <!-- todo: py-[] -->
      <div class="2xl:container 2xl:mx-auto flex justify-center items-center">
        <div
          class="w-96 md:w-auto relative flex flex-col justify-center items-center bg-white py-20 md:py-14 lg:py-16 xl:py-20 px-4 md:px-24 xl:px-30">
          <div>
            <img class="w-20 lg:w-28 select-none" src="@/assets/img/banner.webp" alt="">
          </div>
          <div class="mt-12 md:mt-8 lg:mt-12">
            <h1 class="text-3xl lg:text-4xl font-semibold leading-7 lg:leading-9 text-center text-gray-800 select-none">
              白一面</h1>
          </div>
          <div class="mt-6 md:mt-4">
            <p class="sm:w-80 text-base  leading-7 text-center text-gray-800 select-none">制作: かい</p>
            <p class="sm:w-80 text-base  leading-7 text-center text-gray-800 select-none">注意事項: 白には触れない</p>
          </div>
          <button @click="showStartModal = false"
            class="w-full sm:w-auto mt-12 md:mt-8 lg:mt-12 text-base leading-4 text-center text-white py-3 md:py-4 md:py-4 px-20 md:px-24 bg-gray-800 hover:bg-gray-900 select-none">スタート</button>
        </div>
      </div>
    </div>
  </div>


</template>

<style>
body {
  background-color: black;
  color: white;
  overflow: hidden;
}
</style>


<style scoped>
.main-wrapper {
  height: 100vh;
  height: 100dvh;
  width: 100vw;
}
</style>