<template>
  <transition name="page">
    
    <div class="fixed top-0 w-full blurm bg-opacity-50 z-90" v-show="Show">
      <div class="relative min-h-screen bg-white bg-opacity-25 flex justify-center items-end lg:px-0 ">
        <div class="bg-white w-full md:w-3/4 shadow-2xl xl:w-3/4 h-screen lg:mt-16 lg:mt-28 flex justify-center lg:rounded-t-2xl items-end top-0">
        <transition name="page">

          <div v-show="Show" :class="MaxWidth" class="z-110 relative bottom-0 overflow-hidde sm:rounded-t-3xl h-full w-full md:max-w-7xl">    
            <div class="top-0 z-50 px-4 w-full sm:px-6 flex items-center justify-between border-b border-primary-100 shadow-sm">
              <div class="font-bold text-base sm:text-xl md:text-2xl py-6 md:px-6 mr-2">
                <slot name="title"></slot>
              </div>
              <div class="">
                <div v-if="!HideClose"  @click="$emit('cancel')" class="cursor-pointer hover:shadow-xl">
                  <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="25pt" height="25pt" viewBox="0 0 64 64" version="1.1">
                    <g id="surface1">
                    <path style="stroke:none;fill-rule:nonzero;fill:#b20059;fill-opacity:1;" d="M 10 10 L 10 54 L 54 54 L 54 10 Z M 14 14 L 50 14 L 50 50 L 14 50 Z M 23.375 20.625 L 
                    20.5625 23.4375 L 29.125 32 L 20.4375 40.6875 L 23.25 43.5 L 31.9375 34.8125 L 40.5625 43.4375 L 43.375 40.625 L 34.75 32 L 43.25 23.5 L 40.4375 20.6875 L 31.9375 
                    29.1875 Z "/>
                    </g>
                  </svg>
                </div>
              </div>
              
            </div>
            
            <div class="">
              <div class="w-full px-4 sm:px-6 custom-scroll-y h-screen-80 md:h-screen-75">
                <div class="py-4 md:px-4 text-sm sm:text-base">
                  <slot></slot>
                </div>
              </div>
            </div>
          </div>

        </transition>
        </div>
      </div>
    </div>
    
  </transition>
</template>

<script>
export default {
  
  props: {
    HideClose: Boolean,
    HideFooter: {
      default: false,
      type:Boolean,
    },
    MaxWidth: {
      default: 'md:w-full',
      type: String
    },
    
    SuccessButtonText: String,
    FormButton: Boolean,
    Show:Boolean,
  },

}
</script>

<style>


.blurm{
  background:rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(6px);
  height: 100%;
}
.custom-scroll-y{
  overflow-y: scroll;     
}

.custom-scroll-y::-webkit-scrollbar {
    width:5px;
    background-color: #fff;
    border:1px solid rgb(238, 233, 233);
}

.custom-scroll-y::-webkit-scrollbar-thumb {
    width:5px;
    border-radius: 20%;
    background-color: #9FA25A;
}
.h-screen-80{
  height: 80vh;
}
.h-screen-75{
  height: 75vh;
}

.m-responsive {
  min-height:80%;
}

@media screen and (max-width:768px)
{ 
  .m-responsive {
    min-height:80px;
  }
}

</style>
