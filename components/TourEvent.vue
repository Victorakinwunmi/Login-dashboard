<template>
    <div class="bg-no-repeat bg-cover mb-2 lg:mb-0 bg-top rounded-xl cursor-pointer" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' + tour_event.picture + ')' } ">
        <div class="relative z-0 py-44 hover:bg-black hover:bg-opacity-50 transition duration-500 ease-in-out bg-gradient-to-b from-transparent to-gray-900 rounded-xl">
            <div class="text-white absolute bottom-0 py-4 px-8 md:px-2 w-full h-24 block">
                    <div class="w-full">
                        <p class="text-base w-full truncate">{{tour_event.text}}</p>
                        <button @click="$emit('is_clicked', tour_event)" class="text-sm border mt-2  py-1 px-2 rounded-md hover:bg-gray-400 hover:border-gray-400 duration-500 ease-in-out ">Read more</button>
                    </div>
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
</style>