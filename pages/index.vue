<template>
  <div class="">
      <HeaderLogoMenu/>

      <BigModal :Show="event_tour_modal" @cancel="closeTourEventModal">
        <template #title>{{selected_event_tour.title}}</template>
        <div class="block lg:flex items-center h-full">
           <div class="group bg-no-repeat bg-cover bg-top py-60 rounded-xl lg:py-72 w-full lg:w-4/6 mr-4 mb-4 shadow-xl" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' + selected_event_tour.picture +')' }"></div>
           <div class="w-full lg:w-4/6 lg:ml-10">
             <div class="font-bold text-xl lg:text-2xl mb-6 text-primary-400">{{selected_event_tour.subtitle}}</div>
             <div class="text-lg"> {{selected_event_tour.text}}</div>
           </div>
        </div>
      </BigModal>
      <div class="block w-full pb-0 py-44 bg-primary-400">
        <div class="mx-auto container gap-6 lg:flex justify-between items-center">
            <div class=" max-w-md mx-auto w-full lg:mx-0 lg:w-5/12">
              <h1 class="font-semibold text-center lg:text-left mb-4 lg:mb-8 text-3xl lg:text-4xl text-white">Welcome to </h1>
              <h1 class="font-bold text-white text-center w-full lg:text-left text-4xl md:text-5xl lg:text-6xl">RENAISSANCE INSTRUCTORS</h1>
            </div> 
            <div class="w-full lg:w-7/12 mt-10 lg:mt-0"> 
              <div class="bg-no-repeat h-screen lg:-mt-28 bg-cover w-full mx-auto md:max-w-4xl bg-center" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +require('@/assets/image/callta2.JPG')+ ')' } ">
              </div>
            </div>
        </div>
          
      </div>

      <div class="bg-primary-300 py-16 w-full" id="about">
          <div class="px-4 lg:px-0 mx-auto container">
             <h1 class="font-bold text-2xl lg:text-4xl mb-4 lg:mb-6 text-center lg:text-left text-secondary-500">AT A GLANCE</h1>
            <div>
              <p class="text-secondary-500 text-lg lg:text-2xl leading">Renaissance instructors is a non governmental organization which is made up of consortium of impactful and energetic youths in Iwo land</p>
              <p :class="show_info?'text-secondary-500 text-lg mt-2 lg:text-2xl leading':'hidden'">It was inaugurated on Thursday 17th August, 2017 at the Nulge hall of Iwo local government Secretariat with about 15 people in attendance with the holy mission of encouraging disadvantaged brilliant indigent students  and appreciating our teachers (retired and active)</p>
              <button :class="show_info?'hidden':'block'" @click="showText" class="text-gray-500 focus:text-black text-base lg:text-xl mt-2">Show more</button>
              <button  :class="show_info?'block':'hidden'"  @click="hideText" class="text-gray-500 focus:text-black text-base lg:text-xl mt-2">Show less</button>
            </div>
          </div>
      </div>

      <div class=" py-10 md:py-20 px-6 md:px-0">
         <h1 class="text-secondary-500 lg:px-28 font-bold text-lg text-center mb-4 lg:mb-10 lg:text-4xl">OUR TOUR EVENTS</h1>
         <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-5 container mx-auto gap-4 md:px-10 lg:px-0">
           <TourEvent @is_clicked="showEventTourDetails" v-for="item in events" :key="item.id" :tour_event="{text: item.text, picture: item.img, title:item.title, subtitle:item.subtitle}"
           />
         </div>
      </div>

      <div class="bg-no-repeat bg-cover bg-center" :style="{backgroundRepeat: 'no-repeat' + ';' , backgroundImage: 'url(' + require('@/assets/image/alma.jpg') +')'}">
        <div class="bg-black bg-opacity-70 px-6 lg:px-0 mx-auto py-8 lg:py-28">
          <h1 class="font-bold px-8 mt-6 lg:mt-0 text-center text-lg lg:text-4xl text-white">OUR SERVICES</h1>
          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 container mx-auto gap-2 md:gap-6 md:px-10 lg:px-0">
            <OurServices v-for="item in services" :key="item.id" 
              :icon="item.icon"
              :desc="item.desc"
            /> 
          </div>
        </div>
      </div>

      <div class="w-full bg-gray-400">
          <div class="text-black text-7xl w-full"></div> 
             <VueSlickCarousel v-bind="settings">
                <div class="">
                  <div class="bg-no-repeat bg-cover w-full bg-top" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +require('@/assets/image/karimamodal.jpg')+ ')' } ">
                   <div class="bg-black bg-opacity-40 py-56 lg:py-60"></div>
                  </div>
                </div>
                <div class="">
                    <div class="bg-no-repeat bg-cover bg-top" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +require('@/assets/image/iwomodal.jpg')+ ')' } ">
                      <div class="bg-black bg-opacity-40 py-56 lg:py-60"></div>
                    </div>
                </div>
                <div class="">
                    <div class="bg-no-repeat bg-cover bg-top" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +require('@/assets/image/aipatemodal.jpg')+ ')' } ">
                     <div class="bg-black bg-opacity-40 py-56 lg:py-60"></div>
                    </div>
                </div>
                <div class="">
                    <div class="bg-no-repeat bg-cover bg-top" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +require('@/assets/image/highschlmodal.jpg')+ ')' } ">
                     <div class="bg-black bg-opacity-40 py-56 lg:py-60"></div>
                    </div>
                </div>
                <div class="">
                    <div class="bg-no-repeat bg-cover bg-top" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +require('@/assets/image/a1modal.jpg')+ ')' } ">
                      <div class="bg-black bg-opacity-40 py-56 lg:py-60"></div>
                    </div>
                </div>
                <div class="">
                    <div class="bg-no-repeat bg-cover bg-top" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +require('@/assets/image/iwomodal.jpg')+ ')' } ">
                      <div class="bg-black bg-opacity-40 py-56 lg:py-60"></div>
                    </div>
                </div>
              </VueSlickCarousel>
           <div>
        </div>
      </div>

      <Footer/>
    </div>
    
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'


export default {
 name: 'MyComponent',
components: { VueSlickCarousel },

data(){
    return{
      show_info:false,
      selected_event_tour: '',
      event_tour_modal: false,
      settings:{
        "arrows": false,
        "dots": false,
        "infinite": true,
        "slidesToShow": 3,
        "slidesToScroll": 1,
        "autoplay": true,
        "speed": 10000,
        "autoplaySpeed": 2000,
        "cssEase": "linear",
        "responsive": [
    {
      "breakpoint": 1024,
      "settings": {
        "slidesToShow": 2,
        "slidesToScroll": 1,
        "infinite": true,
        "autoplay": true,
        "speed": 10000,
        "autoplaySpeed": 2000,
        "cssEase": "linear",
        
      }
    },
    {
      "breakpoint": 600,
      "settings": {
        "slidesToShow": 1,
        "slidesToScroll": 1,
        "infinite": true,
        "autoplay": true,
        "speed": 10000,
        "autoplaySpeed": 2000,
        "cssEase": "linear",
      }
    },
    {
      "breakpoint": 480,
      "settings": {
        "slidesToShow": 1,
        "slidesToScroll": 1,
        "infinite": true,
        "autoplay": true,
        "speed": 10000,
        "autoplaySpeed": 2000,
        "cssEase": "linear"
      }
    }
   ]
      },
      events:[
        {
          id:1,
          img:require('@/assets/image/orphan.jpg'),
          text:" In 2017, during our tour of  some growing schools in Iwo land, we came across Karima Ambali, an Orphan with a great academic potentiality. We paid her school fees and render other soft succour to her some other times. It was indeed fulfilling. We make tour to the school back again around 2017 and inspired the students and have them books for self improvement",
          title:'Karima Ambali',
          subtitle:'2017'
        },
         {
          id:2,
          img:require('@/assets/image/highschl.jpg'),
          text:"In 2018, we visited Baptist high school and donated books, school bags  and scholarships to indigent students and reward Late Baba Owojori L. O and anoter female teacher of the year with an award plaques. It was indeed fulfilling",
          title:'Baptist High School',
          subtitle:'2018'
        },
         {
          id:3,
          img:require('@/assets/image/aipate.jpg'),
          text:"In 2019, we visited Aipate Baptist Church Grammar school and donated over 300 customised books and school bags for the junior section while we engage them with life changing seminars ",
          title:'Aipate Baptist Church Grammar School ',
          subtitle:'2019'
        },
         {
          id:4,
          img:require('@/assets/image/iwogram.jpg'),
          text:"In 2020, we visited Iwo Grammar school and donated over 500 customised books, school bags and organized quiz competition while our teacher of the year was Baba kunle Lawal who is a former principal of the school",
          title:'Iwo Grammar School',
          subtitle:'2020'
        },
        {
          id:5,
          img:require('@/assets/image/a1.jpg'),
          text:"  In 2021, The Renaissance instructors conference was set up at A1 comprehensive Grammar school with the theme Total education and talks like effects of drug Abuse by Dr. Abolude while Mr Asifat Omowunmi Morenikeji talked about enterpreneur and students. Elder Amos Idowu, Deacon Victor Idowu and professor Lasisi were our teachers of the year. Students were given awards, bags and other soft items",
          title:' A1 comprehensive Grammar School',
          subtitle:'2021'
        },
      ],
      services:[
        {
          id:1,
          icon:require('@/assets/icon/one.png'),
          desc:'We have the battle of wits quiz competition'
        },
        {
          id:2,
          icon:require('@/assets/icon/two.png'),
          desc:'  Give award to the best three schools from the competition'
        },
        {
          id:3,
          icon:require('@/assets/icon/three.png'),
          desc:'Appreciate dedicated teachers, usually teacher of the year'
        },
        {
          id:4,
          icon:require('@/assets/icon/four.png'),
          desc:'Give a lecture on health and academics'
        },
      ]
 
    };
  },


  methods:{

    showEventTourDetails(item) {
      this.selected_event_tour = item
      this.event_tour_modal =  true
    },

    showText(){
      this.show_info=!this.show_info
    },
    hideText(){
      this.show_info=!this.show_info
    },
   closeTourEventModal(){
    this.event_tour_modal=!this.event_tour_modal
   }
    
    
  },
}


   

</script>

<style>
</style> 