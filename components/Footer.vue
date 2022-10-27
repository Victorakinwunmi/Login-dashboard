<template>
    <div class="bg-secondary-500">
      <div class="py-8 px-10 lg:px-0 md:py-16 container mx-auto w-full bg-secondary-500">
         <div class="ml-0 w-full block md:flex justify-between">
            <div class="w-full md:w-4/12">
              <h1 class="text-white font-bold text-xl lg:text-2xl mb-6">OUR ORGANIZATION</h1>
              <div class="text-white font-normal">
                <button @click=" scrollToAbout()" class="block mb-4">About Us</button>
                <button @click="scrollToService()"  class="hidden lg:block mb-4">Our Services</button>
                <button @click="scrollToServiceMobile()"  class="block lg:hidden mb-4">Our Services</button>
                <button @click="scrollToTour()" class="hidden lg:block mb-4">Our Tour Events</button>
                 <button @click="scrollToTourMobile()" class="block mb-4 lg:hidden">Our Tour Events</button>
              </div>
            </div>
            <div class="w-full md:w-4/12">
              <h1 class="text-white font-bold text-xl lg:text-2xl mb-6">FOLLOW US</h1>
              <div class="text-white font-normal">
                <a href="http://www.facebook.com/Renaissanceinstructors" class="block mb-4">Facebook</a>
                <a href="mailto:wahabsegunjohn@gmail.com?" target="_blank"  class="block mb-4">Email</a>
              </div>
            </div>
            <div class="w-full md:w-4/12">
              <h1 class="text-white font-bold text-xl lg:text-2xl mb-6">TELEPHONE</h1>
              <p class="text-white mb-4 font-semibold">Nigeria (call and WhatsApp)</p>
              <div class="text-white font-normal">
                <div class="flex mb-2">
                    <div class=" mr-4 mb-2">08033089829</div>
                    <div class=" mb-2">08132950588</div>
                </div>
                <div class="flex mb-4">
                   <div class="mr-4">08143137880</div>
                   <div class="">07065317488</div>
                </div>
                <h1 class="text-white mb-4 font-semibold">UK (WhatsApp Only)</h1>
                 <div>+447574907384</div>
              </div>
            </div>
         </div>   
      </div>
    </div>
</template>

<script>
export default {
methods:{
     scrollToTour(){
      window.scroll({top:1000 ,behavior:'smooth'})
    },
    scrollToService(){
      window.scroll({top:1700, behavior:'smooth'})
    },
    scrollToAbout(){
      window.scroll({top:400 ,behavior:'smooth'})
    },
    scrollToTourMobile(){
      window.scroll({top:750 ,behavior:'smooth'})
    },
    scrollToServiceMobile(){
      window.scroll({top:2700 ,behavior:'smooth'})
    }
}
}
</script>

<style>

</style>