<template>
  <div class="flex justify-center items-center rounded-3xl w-full h-44 shadow-2xl">

     <div class="mx-8 xl:mx-2">
        <slot name="icon"></slot>
     </div>

     <div>
        <slot name="details"></slot>
     </div>


     

  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>