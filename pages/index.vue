<template>
  <div class="">
      <HeaderLogoMenu/>

      <BigModal :Show="event_tour_modal" @cancel="closeTourEventModal">
        <template #title>{{selected_event_tour.title}}</template>
        <div class="block lg:flex items-center h-full">
           <div class="group bg-no-repeat bg-cover bg-center py-72 w-full lg:w-4/6 mr-4 mb-4 shadow-xl" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' + selected_event_tour.picture +')' }"></div>
           <div class="w-full lg:w-4/6 lg:ml-10">
             <div class="font-bold text-xl lg:text-2xl mb-6 text-primary-400">{{selected_event_tour.subtitle}}</div>
            {{selected_event_tour.text}}

           </div>
        </div>
      </BigModal>
      <div class="block w-full lg:flex justify-between items-center pb-0 py-44 bg-primary-400">
        <div class=" max-w-md mx-auto w-full lg:mx-0 lg:px-28 lg:w-6/12">
          <h1 class="font-semibold text-center lg:text-left mb-4 lg:mb-8 text-3xl lg:text-5xl text-secondary-500">Welcome to </h1>
          <h1 class="font-bold text-secondary-500 text-center w-full lg:text-left text-4xl md:text-5xl lg:text-6xl">RENAISSANCE INSTRUCTORS</h1>
        </div> 
        <div class="w-full lg:w-6/12 mt-10 lg:mt-0"> 
            <div class="bg-no-repeat bg-cover py-56 lg:h-screen lg:-mt-44 bg-center" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +require('@/assets/image/img1.jpg')+ ')' } "></div>
         
         </div>
          
      </div>

      <div class="bg-primary-300 py-16 px-4 lg:px-28 w-full" id="about">
        <h1 class="font-bold text-2xl lg:text-4xl mb-4 lg:mb-6 text-center lg:text-left text-secondary-500">AT A GLANCE</h1>
        <div>
            <p class="text-secondary-500 text-base lg:text-2xl leading">Renaissance instructors is a non governmental organization which is made up of consortium of impactful and energetic youths in Iwo land</p>
            <p :class="show_info?'text-secondary-500 text-base mt-2 lg:text-2xl leading':'hidden'">It was inaugurated on Thursday 17th August, 2017 at the Nulge hall of Iwo local government Secretariat with about 15 people in attendance with the holy mission of encouraging disadvantaged brilliant indigent students  and appreciating our teachers (retired and active)</p>
            <button :class="show_info?'hidden':'block'" @click="showText" class="text-green-900 text-base mt-2">Show more</button>
            <button  :class="show_info?'block':'hidden'"  @click="hideText" class="text-green-900 text-base mt-2">Show less</button>
        </div>
      </div>

      <div class=" py-10 md:py-20 px-6 md:px-0">
         <h1 class="text-secondary-500 lg:px-28 font-bold text-lg text-center mb-4 lg:mb-10 lg:text-4xl">OUR TOUR EVENTS</h1>
         <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-5 lg:max-w-7xl mx-auto gap-4 md:px-10 lg:px-0">
           <TourEvent @is_clicked="showEventTourDetails" v-for="item in events" :key="item.id" :tour_event="{text: item.text, picture: item.img, title:item.title, subtitle:item.subtitle}"
           />
         </div>
      </div>
:
      <div class="py-10 md:py-20 px-6 md:px-0">
        <h1 class="font-bold px-8 mt-6 lg:mt-0 text-center text-lg lg:text-4xl text-secondary-500">OUR SERVICES</h1>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 max-w-7xl mx-auto gap-6 md:px-10 lg:px-0">
           <OurServices v-for="item in services" :key="item.id" 
            :icon="item.icon"
            :desc="item.desc"
           /> 
        </div>
      </div>
      

      


      <div class="bg-gray-200 w-full py-10 ">
        <h1 class="font-bold text-center text-lg text-secondary-500 lg:px-28 text-lg text-center mb-4 mb-8 lg:text-4xl ">GALLERY</h1>
          <div class="text-black text-7xl"></div>
      </div>

    <Footer/>
  </div>


</template>

<script>
export default {
data(){
    return{
      show_info:false,
      selected_event_tour: '',
      event_tour_modal: false,
     
      events:[
        {
          id:1,
          img:require('@/assets/image/orphan.jpg'),
          text:" In 2017, during our tour of  some growing schools in Iwo land, we came across Karima Ambali, an Orphan with a great academic potentiality. We paid her school fees and",
          title:'Karima Ambali',
          subtitle:'2017'
        },
         {
          id:2,
          img:require('@/assets/image/highschl.jpg'),
          text:"In 2018, we visited Baptist high school and donated books, school bags  and scholarships to indigent students and reward Late Baba Owojori L. O ",
          title:'Baptist High School',
          subtitle:'2018'
        },
         {
          id:3,
          img:require('@/assets/image/aipate.jpg'),
          text:"In 2019, we visited Aipate Baptist Church Grammar school and donated over 300 customised books and school bags for the junior section while we engage them ",
          title:'Aipate Baptist Church Grammar School ',
          subtitle:'2019'
        },
         {
          id:4,
          img:require('@/assets/image/iwogram.jpg'),
          text:"In 2020, we visited Iwo Grammar school and donated over 500 customised books, school bags and organized quiz competition while our teacher of the year was Baba kunle Lawal",
          title:'Iwo Grammar School',
          subtitle:'2020'
        },
        {
          id:5,
          img:require('@/assets/image/a1.jpg'),
          text:"  In 2021, The Renaissance instructors conference was set up at A1 comprehensive Grammar school with the theme Total education and talks like effects of drug Abuse by Dr. Abolude ",
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
      console.log(item)
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