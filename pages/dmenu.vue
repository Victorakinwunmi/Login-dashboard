<template>
  <div class="bg-black h-screen">
      <DropMenu/>
        <div class="flex w-full pt-44 px-28 items-center">
                <div class="w-2/4">
                    <h1 class="text-white text-xl font-semibold mb-6 text-yellow-500">Hello !</h1>
                    <h1 class="text-white text-4xl font-bold mb-2">I Am Victor Adedapo</h1>
                    <p class="text-white">Lorem ipsum dolor sit amet consectetur adipisicing elit. Blanditiis accusantium quibusdam quod ullam dolorum harum earum facere sed praesentium asperiores tenetur, provident aut impedit! Accusamus soluta beatae placeat assumenda sapiente.</p>
                    <div class="mt-4">
                        <button class="text-white py-4 px-8 rounded-full bg-yellow-500">learn More</button>
                        <button class="text-white py-4 px-8 rounded-full ml-2 bg-yellow-500">Hire me</button>
                    </div>
                </div>
                <div class="w-2/4"> 
                <img :src="require('@/assets/image/cta.png')" class="w-10/12 -mt-28">
                </div>
        </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>