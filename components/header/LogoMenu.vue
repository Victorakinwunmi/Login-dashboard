<template>
  <div class="flex justify-between px-8 fixed w-full lg:px-16 items-center blur h-20">
     <div class="w-28 md:w-44 block bg-white rounded-full border-2 mt-16 md:mt-28">
        <img :src="require('@/assets/image/brandlogo.png')" class="">
     </div>
    <div class="">
        <div :class="is_revealed ? 'hidden' : 'block lg:hidden'" @click="showMenu" class="">
           <img :src="require('@/assets/icon/menu.png')" class="w-10 mt-1">
       </div>
       <div :class="is_revealed ? 'block' : 'hidden lg:hidden'" @click="hideMenu" class="">
           <img :src="require('@/assets/icon/close.png')" class="w-10 mt-1">
       </div>
    </div>
    <div :class="
        is_revealed ? 'block top-16 right-0 p-10 w-full h-screen absolute bg-gradient-to-t from-primary-100 to-white ': 'hidden lg:flex lg:w-7/12 lg:justify-end'
      " class="lg:flex lg:items-center cursor-pointer">
        <nuxt-link to="/" class=" text-lg lg:mr-2 font-semibold text-secondary-100 py-2 mt-10 lg:mt-0 px-4 hover:bg-opacity-80 lg:hover:bg-opacity-20 rounded-md hover:bg-gray-400 transition duration-500 ease-in-out"> Home</nuxt-link>
        <div class="flex items-center w-36 lg:w-32 text-secondary-100 text-secondary-100 py-2 px-4 mt-6 lg:mt-0 hover:bg-opacity-80 lg:hover:bg-opacity-20 rounded-md hover:bg-gray-400 transition duration-500 ease-in-out">
            <nuxt-link to="projects" class="text-lg mr-2 font-semibold ">Events</nuxt-link>
            <img :src="require('@/assets/icon/chev_right.png')" class="w-5 mt-1">
        </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      is_revealed: false,
    };
  },

  methods: {
    showMenu() {
      this.is_revealed = true;
    },
    hideMenu() {
      this.is_revealed = false;
    },
  }

};

</script>

<style>
.blur{
  background:rgba(162, 164, 87, 0.1);
  backdrop-filter: blur(10px);
}
</style>