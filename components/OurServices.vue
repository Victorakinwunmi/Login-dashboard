<template>
   <div class="">
    <div class="border mx-auto border-gray-500 h-52 mt-6 lg:mt-10 py-10 px-8 rounded-2xl bg-white shadow-2xl">
        <img :src="icon" class="mx-auto w-16">
        <div class="border-2 border-b mt-2"></div>
        <h1 class="text-base font-bold text-gray-500 text-center mt-2">
        {{desc}}
        </h1>
    </div>
   </div>
</template>

<script>
export default {
   props:{
    icon:String,
    desc:String,
   }
}
</script>

<style>

</style>