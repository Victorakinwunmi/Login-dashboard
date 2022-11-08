<template>
   <div class="relative group flex items-end rounded-2xl overflow-hidden z-0 cursor-pointer bg-gradient-to-b from-transparent to-gray-900 rounded-xl"  @click="$emit('is_clicked', tour_event)" >
        <div class="py-44 bg-gradient-to-b w-full from-transparent to-gray-900"></div>
        <div class="h-full absolute w-full bg-cover scale bg-center overflow-hidden transition duration-1000 ease-in-out rounded-xl cursor-pointer "
                :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' + tour_event.picture+ ')' }">
                 <div class="py-44 bg-gradient-to-b w-full from-transparent transition duration-500 ease-in-out hover:bg-black hover:bg-opacity-50 to-gray-900"></div>
        </div>
        <div class="">
            <div
                class="rounded-2xl bg-gradient-to-b w-full from-transparent text-white to-gray-900 px-1 py-4 bottom-0 w-full h-full duration-500 ease-in-out transform ">
                <div class="font-medium border-l-2 border-white text-base px-2 max-w-sm md:max-w-xs lg:w-72 truncate">{{tour_event.text}}</div>
                <button class="mt-2 border rounded-xl p-2 text-sm border-white hover:bg-gray-500 duration-500 ease-in-out ">Read more</button>
            </div>
        </div>
   </div>
</template>

<script>
export default {
    props:{
        tour_event: {
            type: Object,
        }
    }
};
</script>

<style>
 .scale:hover{
    transform: scale(1.3);
 }
</style>