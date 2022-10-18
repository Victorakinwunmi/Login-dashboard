<template>
  <div>
    <div class="flex justify-between items-center dropbg fixed w-full ">
      <div class="font-black w-6/12 font-mono text-3xl py-3 px-10">LOGO</div>
      <div class=" flex w-6/12 justify-center items-center">
        <div class="relative px-2">
            <button class="font-bold hover:bg-gray-400 p-2 rounded-xl duration-500 ease-in-out transition" @click="dropdownBtn()"  @blur="blur()">Projects</button>
            <div :class="show_dropdown? 'absolute block rounded-lg w-44 top-12 right-0 mx-2 py-3 bg-white':'hidden'">
              <a href="" class="block font-semibold py-2 hover:bg-gray-400 w-full hover:text-white px-4 ">Aipate 2017</a>
              <a href="" class="block font-semibold py-2 hover:bg-gray-400 w-full hover:text-white px-4 ">High school 2018</a>
              <a href="" class="block font-semibold py-2 hover:bg-gray-400 w-full hover:text-white px-4 ">Alma rohm 2019</a>
            </div>
        </div>
        <div class="relative px-2">
            <button class="font-bold hover:bg-gray-400 w-full p-2 rounded-xl duration-500 ease-in-out transition" @click="secondDropdown()" @blur="blur()">Classes</button>
            <div :class="second_dropdown? 'absolute block rounded-lg w-44 top-12 right-0 mx-2 py-3 bg-white':'hidden'">
              <a href="" class="block font-semibold py-2 hover:bg-gray-400 w-full hover:text-white px-4 text-center ">SS1</a>
              <a href="" class="block font-semibold py-2 hover:bg-gray-400 w-full hover:text-white px-4 text-center ">SS2</a>
              <a href="" class="block font-semibold py-2 hover:bg-gray-400 w-full hover:text-white px-4 text-center ">SS3</a>
            </div>
        </div>

      </div>
      
    </div>
  </div>
</template>

<script>
export default {
data(){
    return{
      show_dropdown:false,
      second_dropdown:false,
    }
},
methods:{
  dropdownBtn(){
    this.show_dropdown=!this.show_dropdown
  },
  secondDropdown(){
    this.second_dropdown=! this.second_dropdown
  },
  blur(){
    this.show_dropdown=false,
    this.second_dropdown=false
  }

}
}
</script>

<style>
.dropbg{
  background:rgba(255,255,255, 0.1);
  backdrop-filter: blur(16px);
}
</style>