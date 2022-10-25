<template>
   <div class="">
    <div class="border mx-auto  h-48 mt-6 lg:mt-10 py-10 px-8 rounded-xl bg-gray-300 shadow-xl">
        <img :src="icon" class="mx-auto w-16">
        <h1 class="text-base font-bold text-secondary-100 text-center mt-2">
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