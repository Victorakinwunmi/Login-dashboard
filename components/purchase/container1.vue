<template>
  <div
    class="mt-16 border border-white bg-white shadow-2xl h-4/5 rounded-3xl p-5"
  >
    <div class="flex justify-between items-center">
      <div>
        <div class="text-black font-bold text-3xl">{{ price }}</div>
      </div>

      <div class="flex">
        <div class="border rounded-full bg-black w-2 h-2"></div>
        <div class="border rounded-full bg-black w-2 h-2"></div>
        <div class="border rounded-full bg-black w-2 h-2"></div>
      </div>
    </div>

    <div class="mt-10">
      <h1 class="text-gray-600 font-semibold leading-tight truncate">{{ title }}</h1>
    </div>

    <div class="border border-gray-400 mt-8"></div>

    <div class="flex lg:block xl:flex justify-between items-center mt-10">
      <div>
        <h1 class="font-bold text-xl">{{ desc }}</h1>
      </div>

      
        <button
          class="
            border
            bg-black
            text-gray-300
            font-semibold
            p-3
            text-center
            rounded-full
            flex
            items-center
            lg:mt-5
            xl:mt-0
          "
        >
        <div class="w-full">
          {{ btn }}
        </div>
          <div>
            <img :src="require('@/assets/icons/Arrow.png')" class="w-5 mx-2" />
          </div>
        </button>
     
    </div>
  </div>
</template>

<script>
export default {
  props: {
    price: String,
    title: String,
    desc: String,
    btn: String,
  },
};
</script>

<style>
</style>