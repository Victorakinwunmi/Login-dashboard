<template>
  <div class=" px-8 z-50 fixed w-full lg:px-16 shadow-xl lg:rounded-b-3xl bg-primary-400 h-20">
     <div class="container py-2 flex justify-between z-50 items-center mx-auto">
        <div class="block overflow-hidden w-14 bg-white rounded-full p-1">
         <img :src="require('@/assets/image/brandlogo.png')" class="">
        </div>
        <div class="">
          <div :class="is_revealed ? 'hidden' : 'block lg:hidden'" @click="showMenu" class="">
            <img :src="require('@/assets/icon/menu.png')" class="w-10 z-50">
          </div>
        </div>
        <div :class="is_revealed ? 'block' : 'hidden lg:hidden'" @click="hideMenu" class="">
              <img :src="require('@/assets/icon/close.png')" class="w-10 z-50">
        </div>
        <div :class="
            is_revealed ? 'block top-20 right-0 p-10 w-full justify-between flex h-screen z-50 absolute bg-gradient-to-t from-white to-primary-400 ': 'hidden lg:flex lg:w-7/12 lg:justify-end'
          " class="lg:flex lg:items-center cursor-pointer">
            <div class="block lg:flex -ml-4">
                <nuxt-link to="/" class=" text-2xl lg:text-lg lg:mr-2 font-semibold text-white py-2 mt-10 lg:mt-0 px-4 hover:text-secondary-500  rounded-md transition duration-500 ease-in-out"> Home</nuxt-link>
                <div class="flex items-center lg:w-32 text-white py-2 px-4 mt-6 lg:mt-0 hover:text-secondary-500  rounded-md transition duration-500 ease-in-out">
                    <nuxt-link to="projects" class="text-2xl lg:text-lg mr-2 font-semibold ">Events</nuxt-link>
                    <img :src="require('@/assets/icon/chev_right.png')" class="w-5 mt-1">
                </div>
            </div>
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
  background:hsla(0, 0%, 0%, 0.1);
  backdrop-filter: blur(10px);
}

</style>