<template>
  <div class="">
      <HeaderLogoMenu/>
      <div class="block w-full lg:flex justify-between pb-10 pt-44 px-4 bg-gradient-to-t from-primary-100 to-white lg:px-10 lg:pb-10 lg:pt-40 items-center">
        <div class="md:px-4 lg:px-2 w-full mx-auto lg:w-6/12">
          <h1 class="font-semibold text-center lg:text-left mb-8 text-3xl lg:text-5xl text-secondary-100">Welcome to </h1>
          <h1 class="font-bold text-secondary-100 text-center w-full lg:text-left text-5xl lg:text-7xl">Renaissance instructors</h1>
        </div>
          <img :src="require('@/assets/image/cta.png')" class="w-10/12 md:w-8/12 mx-auto mt-4 lg:mt-0 lg:w-4/12">
      </div>

      <div class="bg-secondary-100 py-16 px-4 lg:px-10 w-full" id="about">
        <h1 class="font-bold text-2xl lg:text-4xl mb-10 text-gray-200">ABOUT</h1>
        <div class=" text-white text-base lg:text-2xl leading">
            Renaissance instructors is a non governmental organization which is made up of consortium of impactful and energetic youths in Iwo land which was inaugurated on Thursday 17th August, 2017 at the Nulge hall of Iwo local government Secretariat with about 15 people in attendance with the holy mission of encouraging disadvantaged brilliant indigent students  and appreciating our teachers (retired and active)
        </div>
      </div>

      <div class="bg-white lg:px-16 lg:py-20" id="service">
          <div class="block rounded-xl bg-gray-100 lg:flex px-8 gap-6 py-10 lg:py-16 lg:px-16">
            <div class="w-full lg:w-8/12 py-4">
              <h1 class="text-secondary-100 font-bold text-lg lg:text-4xl">OUR TOUR EVENTS</h1>
              <div class=" grid-cols-1 grid lg:grid-cols-2 mt-6 lg:mt-10">
                <div class="group bg-no-repeat bg-cover bg-center h-80 mr-4 mb-4 cursor-pointer shadow-xl" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +  require('@/assets/image/orphan.jpg')+ ')' }">
                  <div>
                    <div class="group-hover:opacity-100 duration-500 transition ease-in-out  opacity-0 p-10 text-white bg-black bg-opacity-80 w-full h-80 ">
                        <div class="Font-bold text-base ">
                          <div class="mt-10">
                            In 2017, during our tour of  some growing schools in Iwo land, we came across Karima Ambali, an Orphan with a....
                          </div>
                        </div>
                        <div class="mt-10">
                          <button class="border rounded-full py-2 px-6 font-bold" @click="firstModal">Read more</button>
                        </div>
                    </div>
                  </div>
                </div>
                <div class="group bg-no-repeat bg-cover bg-center h-80 mr-4 mb-4 cursor-pointer shadow-xl" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +  require('@/assets/image/highschl.jpg')+ ')' }">
                  <div>
                    <div class="group-hover:opacity-100 duration-500 transition ease-in-out  opacity-0 p-10 text-white bg-black bg-opacity-80 w-full h-80 ">
                        <div class="Font-bold text-base ">
                          <div class="mt-10">
                            In 2018,we visited Baptist high school and donated books, school bags....
                          </div>
                        </div>
                        <div class="mt-10">
                          <button class="border rounded-full py-2 px-6 font-bold" @click="secondModal">Read more</button>
                        </div>
                    </div>
                  </div>
                </div>
               <div class="group bg-no-repeat bg-cover bg-center h-80 mr-4 mb-4 cursor-pointer shadow-xl" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +  require('@/assets/image/aipate.jpg')+ ')' }">
                  <div>
                    <div class="group-hover:opacity-100 duration-500 transition ease-in-out  opacity-0 p-10 text-white bg-black bg-opacity-80 w-full h-80 ">
                        <div class="Font-bold text-base ">
                          <div class="mt-10">
                           In 2019,we visited Aipate Baptist Church Grammar school and donated over 300....
                          </div>
                        </div>
                        <div class="mt-10">
                          <button class="border rounded-full py-2 px-6 font-bold" @click="thirdModal">Read more</button>
                        </div>
                    </div>
                  </div>
                </div>
                <div class="group bg-no-repeat bg-cover cursor-pointer bg-center h-80 mr-4 mb-4 shadow-xl" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +  require('@/assets/image/img6.jpg')+ ')' }">
                  <div>
                    <div class="group-hover:opacity-100 duration-500 transition ease-in-out  opacity-0 p-10 text-white bg-black bg-opacity-80 w-full h-80 ">
                        <div class="Font-bold text-base ">
                          <div class="mt-10">
                           In 2020 we visited Iwo Grammar school and donated over 500..... 
                          </div>
                        </div>
                        <div class="mt-10">
                          <button class="border rounded-full py-2 px-6 font-bold" @click="fourthModal">Read more</button>
                        </div>
                    </div>
                  </div>
                </div>
                <div class="group bg-no-repeat bg-cover cursor-pointer bg-center h-80 mr-4 mb-4 shadow-xl" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +  require('@/assets/image/a1.jpg')+ ')' }">
                  <div>
                    <div class="group-hover:opacity-100 duration-500 transition ease-in-out  opacity-0 p-10 text-white bg-black bg-opacity-80 w-full h-80 ">
                        <div class="Font-bold text-base ">
                          <div class="mt-10">                         
                             In 2021,The Renaissance instructors conference was set up at A1 comprehensive Grammar school wit...
                          </div>
                        </div>
                        <div class="mt-10">
                          <button class="border rounded-full py-2 px-6 font-bold" @click="fifthModal">Read more</button>
                        </div>
                    </div>
                  </div>
                </div>

              </div>
            </div>
            <div class="block lg:w-4/12">
             <h1 class="font-bold px-8 mt-6 lg:mt-0 text-lg lg:text-2xl text-secondary-100">SERVICES WE OFFER EVERY YEAR</h1>
              <div class="grid grid-cols-1 md:grid-cols-2 gap-2 mx-auto">
                <div class="border mx-auto border-gray-300 mt-6 lg:mt-10 py-10 w-11/12 px-8 rounded-xl bg-gray-200 shadow-xl">
                  <img :src="require('@/assets/icon/one.png')" class="mx-auto w-16">
                  <h1 class="text-base text-secondary-100 font-semibold text-center mt-2">
                    We have the battle of wits quiz competition
                  </h1>
                </div>
                <div class="border mx-auto border-gray-300 mt-6 lg:mt-10 py-10 w-11/12 px-8 rounded-xl bg-gray-200 shadow-xl">
                  <img :src="require('@/assets/icon/two.png')" class="mx-auto w-16">
                  <h1 class="text-base text-secondary-100 font-semibold text-center mt-2">
                   Give award to the best three schools from the competition
                  </h1>
                </div>
                <div class="border mx-auto border-gray-300 mt-6 lg:mt-10 py-10 w-11/12 px-8 rounded-xl bg-gray-200 shadow-xl">
                  <img :src="require('@/assets/icon/three.png')" class="mx-auto w-16">
                  <h1 class="text-base text-secondary-100 font-semibold text-center mt-2">
                  Appreciate dedicated teachers, usually teacher of the year.
                  </h1>
                </div>
                <div class="border mx-auto border-gray-300 mt-6 lg:mt-10 py-10 w-11/12 px-8 rounded-xl bg-gray-200 shadow-xl">
                  <img :src="require('@/assets/icon/four.png')" class="mx-auto w-16">
                  <h1 class="text-base text-secondary-100 font-semibold text-center mt-2">
                  Give a lecture on health and academics
                  </h1>
                </div>
                
              </div>

              <div class="border mx-auto border-gray-200 shadow-xl w-11/12 lg:w-full py-10 px-8 rounded-xl mt-8">
                <h1 class="font-bold text-secondary-100 text-xl">UPCOMING EVENTS</h1>
                <h1 class="mt-4">{{whois[0]}}</h1>
              </div>
            </div>
          </div> 
      </div>
      <BigModal :Show="first_popup" @cancel="firstModal">
        <template #title>OUR TOUR EVENT</template>
        <div class="block lg:flex items-center">
           <div class="group bg-no-repeat bg-cover bg-center h-96 w-full lg:w-6/12 mr-4 mb-4 shadow-xl" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +  require('@/assets/image/orphan.jpg')+ ')' }"></div>
           <div class="w-full lg:w-6/12">
             <div class="font-bold text-xl mb-6">KARIMA AMBALI</div>
             <h1 class="">In 2017, during our tour of  some growing schools in Iwo land, we came across Karima Ambali, an Orphan with a great academic potentiality. We paid her school fees and render other soft succour to her some other times. It was indeed fulfilling..We make a tour to the school back again around 2017 and inspired the students and have them books for self improvement.</h1>
           </div>
        </div>
      </BigModal>
      <BigModal :Show="second_popup" @cancel="secondModal">
        <template #title>OUR TOUR EVENT</template>
        <div class="block lg:flex items-center">
           <div class="group bg-no-repeat bg-cover bg-center h-96 w-full lg:w-6/12 mr-4 mb-4 shadow-xl" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +  require('@/assets/image/highschl.jpg')+ ')' }"></div>
           <div class="w-full lg:w-6/12">
             <div class="font-bold text-xl mb-6">BAPTIST HIGH SCHOOL</div>
             <h1 class="">In 2018, we visited Baptist high school and donated books, school bags  and scholarships to indigent students and reward Late Baba Owojori L. O and another female teacher as our teachers of the year with an award plaques. it was indeed fulfilling.</h1>
           </div>
        </div>
      </BigModal>
      <BigModal :Show="third_popup" @cancel="thirdModal">
        <template #title>OUR TOUR EVENT</template>
        <div class="block lg:flex items-center">
           <div class="group bg-no-repeat bg-cover bg-center h-96 w-full lg:w-6/12 mr-4 mb-4 shadow-xl" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +  require('@/assets/image/aipate3.jpg')+ ')' }"></div>
           <div class="w-full lg:w-6/12">
             <div class="font-bold text-xl mb-6">AIPATE BAPTIST CHURCH GRAMMAR SCHOOL</div>
             <h1 class="">In 2019,we visited Aipate Baptist Church Grammar school and donated over 300 customised books and school bags for the junior section while we engage them with life changing seminars</h1>
           </div>
        </div>
      </BigModal>
      <BigModal :Show="fourth_popup" @cancel="fourthModal">
        <template #title>OUR TOUR EVENT</template>
        <div class="block lg:flex items-center">
           <div class="group bg-no-repeat bg-cover bg-center h-96 w-full lg:w-6/12 mr-4 mb-4 shadow-xl" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +  require('@/assets/image/img6.jpg')+ ')' }"></div>
           <div class="w-full lg:w-6/12">
             <div class="font-bold text-xl mb-6">IWO GRAMMAR SCHOOL</div>
             <h1 class="">In 2020 we visited Iwo Grammar school and donated over 500 customised books, school bags and organized quiz competition while our teacher of the year was Baba kunle Lawal who is a formal principal of the schoolcustomised books and school bags for the junior section while we engage them with life changing seminars</h1>
           </div>
        </div>
      </BigModal>
      <BigModal :Show="fifth_popup" @cancel="fifthModal">
        <template #title>OUR TOUR EVENT</template>
        <div class="block lg:flex items-center">
           <div class="group bg-no-repeat bg-cover bg-center h-96 w-full lg:w-6/12 mr-4 mb-4 shadow-xl" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +  require('@/assets/image/a1.jpg')+ ')' }"></div>
           <div class="w-full lg:w-6/12">
             <div class="font-bold text-xl mb-6">A1 GRAMMAR SCHOOL</div>
             <h1 class="">
                  In 2021,The Renaissance instructors conference was set up at A1 comprehensive Grammar school with the theme Total education and talks like effects of drug Abuse by Dr. Abolude while Mr Asifat omowumi Moronkeji talked about entrepreneur and students. Elder Amos Idowu, Deacon Victor Idowu and professor Lasisi  were our teachers of the year. Students were given awards , bags and other soft items.
                  life changing seminars</h1>
           </div>
        </div>
      </BigModal>

      <div class="bg-gray-200 w-full py-10 px-28">
        <h1 class="text-secondary-100 font-bold text-lg lg:text-3xl mb-8">EVENTS GALLERY</h1>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
           <img :src="require('@/assets/image/img2.jpg')" class="">
           <img :src="require('@/assets/image/img3.jpg')" class="">
           <img :src="require('@/assets/image/img5.jpg')" class="">
           <img :src="require('@/assets/image/img6.jpg')" class="">
        </div>
      </div>

      <div class="py-8 px-14 md:py-16 md:px-16 lg::px-28 mx-auto w-full bg-secondary-100">
         <div class="block md:flex justify-between">
            <div class="w-full md:w-4/12">
              <h1 class="text-white font-bold text-xl lg:text-2xl mb-6">OUR ORGANIZATION</h1>
              <div class="text-white font-normal">
                <div @click=" scrollToAbout()" class="block mb-4">About Us</div>
                <div @click="scrollToTour()"  class="hidden lg:block mb-4">Our Services</div>
                <div @click="scrollToService()"  class="block lg:hidden mb-4">Our Services</div>
                <div @click="scrollToTour()" class="block mb-4">Our Tour Events</div>
              </div>
            </div>
            <div class="w-full md:ml-4 lg:ml-0 md:w-4/12">
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
data(){
    return{
      first_popup:false,
      second_popup:false,
      third_popup:false,
      fourth_popup:false,
      fifth_popup:false,
      
      whois: [
         `Our next program is on Oct 8 at Regina mundi girls secondary school where over 100 students will converge for the battle of wits quiz program and celebrate two outstanding teachers viz`,
         `Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis obcaecati dignissimos expedita illo ipsam velit nobis adipisci unde eveniet dolorem quis nulla mollitia, et necessitatibus sapiente neque magni enim debitis!`,
         `we have a program on Nov 9 at baptist high school iwo where over 500 students will converge for the battle of witz quiz program`
        ]
 
    };
  },

  mounted(){
    window.setInterval(()=>{
      this.pollPerson();
    }, 5000);
  },

  methods:{
     pollPerson(){
      const first = this.whois.shift();
      this.whois = this.whois.concat(first);
    },
    scrollToTour(){
      window.scroll({top:1000 ,behavior:'smooth'})
    },
    scrollToService(){
      window.scroll({top:2800, behavior:'smooth'})
    },
    scrollToAbout(){
      window.scroll({top:400 ,behavior:'smooth'})
    },
    
    firstModal(){
      this.first_popup=!this.first_popup;
    },
    secondModal(){
      this.second_popup=!this.second_popup;
    },
     thirdModal(){
      this.third_popup=!this.third_popup;
    },
    fourthModal(){
      this.fourth_popup=!this.fourth_popup;
    },
    fifthModal(){
      this.fifth_popup =!this.fifth_popup;
    }
  },
}


   

</script>

<style>

</style> 