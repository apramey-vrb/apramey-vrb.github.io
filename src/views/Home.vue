<template>
  <header class="text-gray-600 body-font bg-gradient-to-r from-green-400 to-blue-500 hover:from-pink-500 hover:to-yellow-500 text-gray-800">
        <div class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center">
          <a class="flex title-font font-medium items-center text-gray-900 mb-4 md:mb-0">
            <span class="ml-3 text-xl">🌀 Aprameyoscope</span>
          </a>
          <nav class="md:ml-auto flex flex-wrap items-center text-base justify-center">
            <router-link class="mr-5 hover:text-gray-900 font-semibold" to="/">Home</router-link>
        </nav></div>
  </header>


  <section class="text-gray-600 body-font">
        <div class="container mx-auto flex px-5 py-24 md:flex-row flex-col items-center">
          <div class="lg:flex-grow md:w-1/2 lg:pr-24 md:pr-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center text-center">
            <h1 class="title-font sm:text-4xl text-3xl mb-4 font-medium text-gray-900">Apramey Bhat ⚡
              <br class="hidden lg:inline-block">
            </h1>
            <h3 class="mb-8 leading-relaxed">Hi there!<br>
              Yet another software engineer here!<br>
              Currently building Plymouth at First American<br>
              I love Technology, Photography, Travel and Philosophy </h3>
              <div class="flex mb-4">
                <div class="w-1/3  h-12 "><button class="bg-gradient-to-r from-green-400 to-blue-500 hover:from-pink-500 hover:to-yellow-500 text-gray-800 font-semibold py-2 px-4  rounded shadow" onclick="window.location.href='https://twitter.com/ChhajedViraj';" >
                  Twitter
                </button></div>
                <div class="w-1/3  h-12 mx-3"><button class="bg-gradient-to-r from-green-400 to-blue-500 hover:from-pink-500 hover:to-yellow-500 text-gray-800 font-semibold py-2 px-4  rounded shadow" onclick="window.location.href='https://www.linkedin.com/in/virajchhajed/';" >
                  LinkedIn
                </button></div>
                <div class="w-1/3  h-12"><button class="bg-gradient-to-r from-green-400 to-blue-500 hover:from-pink-500 hover:to-yellow-500 text-gray-800 font-semibold py-2 px-4  rounded shadow" onclick="window.location.href='https://www.instagram.com/viraj.chhajed/';" >
                  Instagram
                </button></div>
              </div>
          </div>
          
          <div class="lg:max-w-lg lg:w-full md:w-1/2 w-5/6">
            
          </div>
          
        </div>
      </section>


      <section class="text-gray-600 body-font">
          
        <div class=" container px-5 py-24 mx-auto">
         
          <CardHeader :items="expHeader"/>

          <div class="flex flex-wrap -m-4">
            <div v-for="ex in experience" v-bind:key="ex.id" class="xl:w-1/4 md:w-1/2 p-4">
               <Card :obj="ex"/>
            </div>
          </div> 
        </div>
       
      </section>
</template>

<script>
// @ is an alias to /src
import Card from "@/components/Card.vue"
import CardHeader from "@/components/CardHeader.vue"

export default {
  name: 'Home',
  data() {
    return{
      experience : [
        {
          id : 1,
          title : "SOFTWARE ENGINEER",
          subtitle : "First American Title Corporation",
          date : "Dec 2020 - Present",
          description : "Part of team <b>TRecS</b> 🐱‍🐉, contributing for Project Plymouth",
          imgsrc : ""
        },
        {
          id : 2,
          title : "TRYING &",
          subtitle : "Learning new things",
          date : "Forever learning",
          description : "I love to explore new stuffs. Investment in knowledge gives best interest! 🖖",
          imgsrc : ""
        },
        {
          id : 3,
          title : "PRODUCT ENGINEER",
          subtitle : "Inszoom",
          date : "Jul 2018 - Dec 2020",
          description : "An immigration case management software ✈",
          pointers : ["Awarded with Zoom Star🥇","Member of Core tech team👨‍💻","Worked, Designed and Delivered in core modules of INSZoom product like Case & KB, Forms, Questionnaires🚀","Actively participated in articulating coding standards and code review document📃","Conducted project training and knowledge sessions for new hires👶"],
          imgsrc : "",
          isPing : true
        },
        {
          id : 4,
          title : "ANDROID DEVELOPMENT INTERN",
          subtitle : "Boredbees tech solutions",
          date : "Jan 2016",
          description : "Built 2 (GRE Made easy, Code baba) android applications 👾 in span of 1 week.",
          imgsrc : ""
        }
      ],
      expHeader : ["Present:","Past:"]
    }
  },
  components: {
    Card,
    CardHeader
  },
};
</script>
