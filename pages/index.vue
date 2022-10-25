<template>
  <div class="">
      <HeaderLogoMenu/>
      <div class="block w-full lg:flex justify-between px-10 items-center pb-10 py-44 bg-primary-100 lg:py-52">
        <div class=" max-w-md mx-auto lg:mx-0 lg:px-20 lg:w-6/12">
          <h1 class="font-semibold text-center lg:text-left mb-8 text-3xl lg:text-5xl text-secondary-100">Welcome to </h1>
          <h1 class="font-bold text-secondary-100 text-center w-full lg:text-left text-4xl lg:text-5xl">RENAISSANCE INSTRUCTORS</h1>
        </div> 
          <img :src="require('@/assets/image/img1.jpg')" class=" w-10/12 md:w-8/12 mt-4 px-2 mx-auto lg:mt-0 lg:w-6/12">
      </div>

      <div class="bg-primary-200 py-16 px-4 lg:px-28 w-full" id="about">
        <h1 class="font-bold text-2xl lg:text-4xl mb-4 lg:mb-6 text-center lg:text-left text-secondary-100">AT A GLANCE</h1>
        <div>
            <p class="text-secondary-100 text-base lg:text-2xl leading">Renaissance instructors is a non governmental organization which is made up of consortium of impactful and energetic youths in Iwo land</p>
            <p :class="show_info?'text-secondary-100 text-base mt-2 lg:text-2xl leading':'hidden'">It was inaugurated on Thursday 17th August, 2017 at the Nulge hall of Iwo local government Secretariat with about 15 people in attendance with the holy mission of encouraging disadvantaged brilliant indigent students  and appreciating our teachers (retired and active)</p>
            <button :class="show_info?'hidden':'block'" @click="showText" class="text-secondary-100 text-base mt-2">Show more</button>
            <button  :class="show_info?'block':'hidden'"  @click="hideText" class="text-secondary-100 text-base mt-2">Show less</button>
        </div>
      </div>

      <div class=" py-10 md:py-20 px-6 md:px-0">
         <h1 class="text-secondary-100 lg:px-28 font-bold text-lg text-center mb-4 lg:mb-10 lg:text-4xl">OUR TOUR EVENTS</h1>
         <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-5 lg:max-w-7xl mx-auto  md:px-10 lg:px-0">
           <TourEvent v-for="item in events" :key="item.id"
             :pic="item.img"
             :text="item.text"
           />
         </div>
      </div>

      <div class="py-10 md:py-20 px-6 md:px-0">
        <h1 class="font-bold px-8 mt-6 lg:mt-0 text-center text-lg lg:text-4xl text-secondary-100">OUR SERVICES</h1>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 max-w-7xl mx-auto md:px-10 lg:px-0">
           <OurServices v-for="item in services" :key="item.id" 
            :icon="item.icon"
            :desc="item.desc"
           /> 
        </div>
      </div>
      

      <BigModal :Show="first_popup" @cancel="firstModal">
        <template #title>OUR TOUR EVENT</template>
        <div class="block lg:flex items-center h-full">
           <div class="group bg-no-repeat bg-cover bg-center h-96 w-full lg:w-2/6 mr-4 mb-4 shadow-xl" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +  require('@/assets/image/karimamodal.jpg')+ ')' }"></div>
           <div class="w-full lg:w-4/6 lg:ml-10">
             <div class="font-bold text-xl lg:text-2xl mb-6 text-primary-100">KARIMA AMBALI</div>
            In 2017, during our tour of  some growing schools in Iwo land, we came across Karima Ambali, an Orphan with a great academic potentiality. We paid her school fees and render other soft succour to her some other times. It was indeed fulfilling..We make a tour to the school back again around 2017 and inspired the students and have them books for self improvement.

           </div>
        </div>
      </BigModal>
      <BigModal :Show="second_popup" @cancel="secondModal">
        <template #title>OUR TOUR EVENT</template>
        <div class="block lg:flex items-center">
           <div class="group bg-no-repeat bg-cover bg-center h-96 w-full lg:w-2/6 mr-4 mb-4 shadow-xl" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +  require('@/assets/image/highschlmodal.jpg')+ ')' }"></div>
           <div class="w-full lg:w-4/6 lg:ml-10">
             <div class="font-bold text-xl lg:text-2xl mb-6 text-primary-100">BAPTIST HIGH SCHOOL</div>
             <h1 class="">In 2018, we visited Baptist high school and donated books, school bags  and scholarships to indigent students and reward Late Baba Owojori L. O and another female teacher as our teachers of the year with an award plaques. it was indeed fulfilling.</h1>
           </div>
        </div>
      </BigModal>
      <BigModal :Show="third_popup" @cancel="thirdModal">
        <template #title>OUR TOUR EVENT</template>
        <div class="block lg:flex items-center">
           <div class="group bg-no-repeat bg-cover bg-center h-96 w-full lg:w-2/6 mr-4 mb-4 shadow-xl" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +  require('@/assets/image/aipatemodal.jpg')+ ')' }"></div>
           <div class="w-full lg:w-4/6 lg:ml-10">
             <div class="font-bold text-xl lg:text-2xl mb-6 text-primary-100">AIPATE BAPTIST CHURCH GRAMMAR SCHOOL</div>
             <h1 class="">In 2019,we visited Aipate Baptist Church Grammar school and donated over 300 customised books and school bags for the junior section while we engage them with life changing seminars</h1>
           </div>
        </div>
      </BigModal>
      <BigModal :Show="fourth_popup" @cancel="fourthModal">
        <template #title>OUR TOUR EVENT</template>
        <div class="block lg:flex items-center">
           <div class="group bg-no-repeat bg-cover bg-center h-96 w-full lg:w-2/6 mr-4 mb-4 shadow-xl" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +  require('@/assets/image/iwomodal.jpg')+ ')' }"></div>
           <div class="w-full lg:w-4/6 lg:ml-10">
             <div class="font-bold text-xl lg:text-2xl mb-6 text-primary-100">IWO GRAMMAR SCHOOL</div>
             <h1 class="">In 2020 we visited Iwo Grammar school and donated over 500 customised books, school bags and organized quiz competition while our teacher of the year was Baba kunle Lawal who is a formal principal of the schoolcustomised books and school bags for the junior section while we engage them with life changing seminars</h1>
           </div>
        </div>
      </BigModal>
      <BigModal :Show="fifth_popup" @cancel="fifthModal">
        <template #title>OUR TOUR EVENT</template>
        <div class="block lg:flex items-center">
           <div class="group bg-no-repeat bg-cover bg-center h-96 w-full lg:w-2/6 mr-4 mb-4 shadow-xl" :style="{ backgroundRepeat: 'no-repeat' + ';', backgroundImage: 'url(' +  require('@/assets/image/a1modal.jpg')+ ')' }"></div>
           <div class="w-full lg:w-4/6 lg:ml-10">
             <div class="font-bold text-xl lg:text-2xl mb-6 text-primary-100">A1 GRAMMAR SCHOOL</div>
             <h1 class="">
                  In 2021,The Renaissance instructors conference was set up at A1 comprehensive Grammar school with the theme Total education and talks like effects of drug Abuse by Dr. Abolude while Mr Asifat omowumi Moronkeji talked about entrepreneur and students. Elder Amos Idowu, Deacon Victor Idowu and professor Lasisi  were our teachers of the year. Students were given awards , bags and other soft items.
                  life changing seminars</h1>
           </div>
        </div>
      </BigModal>

      <div class="bg-gray-200 w-full py-10 ">
        <h1 class="font-bold text-center text-lg text-secondary-100 lg:px-28 text-lg text-center mb-4 mb-8 lg:text-4xl ">GALLERY</h1>
          <div class="text-black text-7xl">carousel</div>
      </div>

    <Footer/>
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
      show_info:false,
     
      
      whois: [
         `Our next program is on Oct 8 at Regina mundi girls secondary school where over 100 students will converge for the battle of wits quiz program and celebrate two outstanding teachers viz`,
         `Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis obcaecati dignissimos expedita illo ipsam velit nobis adipisci unde eveniet dolorem quis nulla mollitia, et necessitatibus sapiente neque magni enim debitis!`,
         `we have a program on Nov 9 at baptist high school iwo where over 500 students will converge for the battle of witz quiz program`
        ],

      events:[
        {
          id:1,
          img:require('@/assets/image/orphan.jpg'),
          text:" In 2017, during our tour of  some growing schools in Iwo land, we came across Karima Ambali, an Orphan with a great academic potentiality. We paid her school fees and",
        },
         {
          id:2,
          img:require('@/assets/image/highschl.jpg'),
          text:"In 2018, we visited Baptist high school and donated books, school bags  and scholarships to indigent students and reward Late Baba Owojori L. O ",
        },
         {
          id:3,
          img:require('@/assets/image/aipate.jpg'),
          text:"In 2019,we visited Aipate Baptist Church Grammar school and donated over 300 customised books and school bags for the junior section while we engage them ",
        },
         {
          id:4,
          img:require('@/assets/image/iwogram.jpg'),
          text:"In 2020 we visited Iwo Grammar school and donated over 500 customised books, school bags and organized quiz competition while our teacher of the year was Baba kunle Lawal",
        },
        {
          id:5,
          img:require('@/assets/image/a1.jpg'),
          text:"  In 2021,The Renaissance instructors conference was set up at A1 comprehensive Grammar school with the theme Total education and talks like effects of drug Abuse by Dr. Abolude ",
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

  mounted(){
    window.setInterval(()=>{
      this.pollPerson();
    }, 5000);
  },

  methods:{
    showText(){
      this.show_info=!this.show_info
    },
    hideText(){
      this.show_info=!this.show_info
    },
     pollPerson(){
      const first = this.whois.shift();
      this.whois = this.whois.concat(first);
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