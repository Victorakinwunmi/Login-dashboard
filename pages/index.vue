<template>
  <div class="">
      <HeaderLogoMenu/>
      <div class="block w-full lg:flex justify-between py-44 px-4 bg-gradient-to-t from-primary-100 to-white lg:px-10 lg:py-40 items-center">
        <div class="md:px-4 lg:px-2 w-full mx-auto lg:w-6/12">
          <h1 class="font-semibold text-center lg:text-left mb-8 text-3xl lg:text-5xl text-secondary-100">Welcome to :</h1>
          <h1 class="font-bold text-secondary-100 text-center w-full lg:text-left text-5xl lg:text-7xl">Renaissance instructors</h1>
        </div>
          <img :src="require('@/assets/image/cta.png')" class="w-10/12 md:w-8/12 mx-auto mt-4 lg:mt-0 lg:w-4/12">
      </div>

      <div class="bg-secondary-100 py-16 px-4 lg:px-10 w-full">
        <h1 class="font-bold text-2xl lg:text-4xl mb-10 text-gray-200">ABOUT</h1>
        <div class=" text-white text-base lg:text-2xl leading">
            Renaissance instructors is a non governmental organization which is made up of consortium of impactful and energetic youths in Iwo land which was inaugurated on Thursday 17th August, 2017 at the Nulge hall of Iwo local government Secretariat with about 15 people in attendance with the holy mission of encouraging disadvantaged brilliant indigent students  and appreciating our teachers (retired and active)
        </div>
      </div>

      <div class="bg-white lg:px-16 lg:py-20">
          <div class="block rounded-xl bg-gray-100 lg:flex px-8 gap-6 py-10 lg:py-16 lg:px-16">
            <div class="w-full lg:w-6/12 py-4">
              <h1 class="text-secondary-100 font-bold text-lg lg:text-4xl">OUR TOUR EVENTS</h1>
              <div class="mt-6 lg:mt-10">
                <div class="mb-4">
                   In 2017, during our tour of  some growing schools in Iwo land, we came across Karima Ambali, an Orphan with a great academic potentiality. We paid her school fees and render other soft succour to her some other times. It was indeed fulfilling..
                  We make a tour to the school back again around 2017 and inspired the students and have them books for self improvement.
                </div>
                <div class="mb-4">
                   In 2018,we visited Baptist high school and donated books, school bags  and scholarships to indigent students and reward Late Baba Owojori L. O and another female teacher as our teachers of the year with an award plaques. it was indeed fulfilling.
                </div>
                <div class="mb-4">
                   In 2019,we visited Aipate Baptist Church Grammar school and donated over 300
                </div>
                <div class="mb-4">
                  In 2020 we visited Iwo Grammar school and donated over 500 customised books, school bags and organized quiz competition while our teacher of the year was Baba kunle Lawal who is a formal principal of the school
                  customised books and school bags for the junior section while we engage them with
                </div>
                <div class="">
                  In 2021,The Renaissance instructors conference was set up at A1 comprehensive Grammar school with the theme Total education and talks like effects of drug Abuse by Dr. Abolude while Mr Asifat omowumi Moronkeji talked about entrepreneur and students. Elder Amos Idowu, Deacon Victor Idowu and professor Lasisi  were our teachers of the year. Students were given awards , bags and other soft items.
                  life changing seminars
                </div>

              </div>
            </div>
            <div class="block lg:w-6/12">
             <h1 class="font-bold mt-2 text-lg lg:text-2xl text-secondary-100">SERVICES THAT WE OFFER EVERY YEAR:</h1>
              <div class="grid grid-cols-1 md:grid-cols-2 gap-2 mx-auto">
                <div class="border mx-auto border-gray-300 mt-6 lg:mt-10 py-10 w-10/12 px-10 rounded-xl bg-gray-200 shadow-xl">
                  <img :src="require('@/assets/icon/one.png')" class="mx-auto w-16">
                  <h1 class="text-base text-secondary-100 font-semibold text-center mt-2">
                    We have the battle of wits quiz competition
                  </h1>
                </div>
                <div class="border mx-auto border-gray-300 mt-6 lg:mt-10 py-10 w-10/12 px-10 rounded-xl bg-gray-200 shadow-xl">
                  <img :src="require('@/assets/icon/two.png')" class="mx-auto w-16">
                  <h1 class="text-base text-secondary-100 font-semibold text-center mt-2">
                   Give award to the best three schools from the competition
                  </h1>
                </div>
                <div class="border mx-auto border-gray-300 mt-6 lg:mt-10 py-10 w-10/12 px-10 rounded-xl bg-gray-200 shadow-xl">
                  <img :src="require('@/assets/icon/three.png')" class="mx-auto w-16">
                  <h1 class="text-base text-secondary-100 font-semibold text-center mt-2">
                  Appreciate dedicated teachers, usually teacher of the year.
                  </h1>
                </div>
                <div class="border mx-auto border-gray-300 mt-6 lg:mt-10 py-10 w-10/12 px-10 rounded-xl bg-gray-200 shadow-xl">
                  <img :src="require('@/assets/icon/four.png')" class="mx-auto w-16">
                  <h1 class="text-base text-secondary-100 font-semibold text-center mt-2">
                  Give a lecture on health and academics
                  </h1>
                </div>
                
              </div>

              <div class="border mx-auto border-gray-200 shadow-xl w-full py-10 px-10 rounded-xl mt-8">
                <h1 class="font-bold text-secondary-100 text-xl">UPCOMING EVENTS</h1>
                <div class="mt-4">Our next program is on Oct 8 at Regina mundi girls secondary school where over 100 students will converge for the battle of wits quiz program and celebrate two outstanding teachers viz;</div>
              </div>
            </div>
          </div> 
      </div>

      <div class="bg-gray-200 w-full py-10 px-28">
        <h1 class="text-secondary-100 font-bold text-lg lg:text-3xl">EVENTS GALLERY</h1>
      </div>
      
  </div>

</template>

<script>
export default {

}
</script>

<style>

</style> 