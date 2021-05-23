<template>
      <header class="text-gray-600 body-font bg-gradient-to-r from-green-400 to-blue-500 hover:from-pink-500 hover:to-yellow-500 text-gray-800">
            <div class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center">
              <a class="flex title-font font-medium items-center text-gray-900 mb-4 md:mb-0">
                <span class="ml-3 text-xl">🌀 Aprameyoscope</span>
              </a>
              <nav class="md:ml-auto flex flex-wrap items-center text-base justify-center">
                <router-link class="mr-5 hover:text-gray-900 font-bold" to="/">Home</router-link>
            </nav></div>
      </header>


      <section class="text-gray-600 body-font">
        <div class="container mx-auto flex px-5 py-24 md:flex-row flex-col items-center">
          <div class="lg:flex-grow md:w-1/2 lg:pr-24 md:pr-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center text-center">
            <h1 class="title-font sm:text-5xl text-5xl mb-4 pt-4 pb-4 font-bold rainbow rainbow_text_animated">Apramey Bhat ⚡
              <br class="hidden lg:inline-block">
            </h1>
            <h3 class="mb-8 leading-relaxed font-semibold">Hi there!<br>
              Yet another software engineer here!<br>
              Currently building Plymouth at First American<br>
              I love Technology, Photography, Travel and Philosophy </h3>
              <div class="flex mb-4">
                <div class="w-1/3  h-12 "><button class="bg-gray-200 hover:bg-blue-500 text-gray-800 font-semibold py-2 px-4  rounded shadow" onclick="window.location.href='https://twitter.com/ChhajedViraj';" >
                  <svg fill="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-5 h-5" viewBox="0 0 24 24">
                    <path d="M23 3a10.9 10.9 0 01-3.14 1.53 4.48 4.48 0 00-7.86 3v1A10.66 10.66 0 013 4s-4 9 5 13a11.64 11.64 0 01-7 2c9 5 20 0 20-11.5a4.5 4.5 0 00-.08-.83A7.72 7.72 0 0023 3z"></path>
                  </svg>
                </button></div>
                <div class="w-1/3  h-12 mx-3"><button class="bg-gray-200 hover:bg-blue-500 text-gray-800 font-semibold py-2 px-4  rounded shadow" onclick="window.location.href='https://www.linkedin.com/in/virajchhajed/';" >
                  <svg fill="currentColor" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="0" class="w-5 h-5" viewBox="0 0 24 24">
                    <path stroke="none" d="M16 8a6 6 0 016 6v7h-4v-7a2 2 0 00-2-2 2 2 0 00-2 2v7h-4v-7a6 6 0 016-6zM2 9h4v12H2z"></path>
                    <circle cx="4" cy="4" r="2" stroke="none"></circle>
                  </svg>
                </button></div>
                <div class="w-1/3  h-12"><button class="bg-gray-200 hover:bg-yellow-500 text-gray-800 font-semibold py-2 px-4  rounded shadow" onclick="window.location.href='https://www.instagram.com/viraj.chhajed/';" >
                  <svg fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-5 h-5" viewBox="0 0 24 24">
                  <rect width="20" height="20" x="2" y="2" rx="5" ry="5"></rect>
                  <path d="M16 11.37A4 4 0 1112.63 8 4 4 0 0116 11.37zm1.5-4.87h.01"></path>
                  </svg>
                </button></div>
              </div>
          </div>
          <div class="lg:max-w-lg lg:w-full md:w-1/2 w-5/6">
          </div>
        </div>
      </section>


      <section class="text-gray-600 body-font">
        <div class=" container px-5 py-24 mx-auto">
          <div class="flex flex-wrap -mx-2 overflow-hidden sm:-mx-1 md:-mx-1 lg:-mx-3 xl:-mx-2">
              <CardHeader :cards="presentExperience" :header="'Present:'" :classNames="experienceClass" />
              <CardHeader :cards="pastExperience" :header="'Past:'" :classNames="experienceClass"/>
          </div>
        </div> 
      </section>
</template>

<script>
// @ is an alias to /src
import CardHeader from "@/components/CardHeader.vue"

export default {
  name: 'Home',
  data() {
    return{
      presentExperience : [
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
        }
      ],
      pastExperience :[
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
      experienceClass : {
        grid : "grid grid-cols-2 px-2 sm:w-full xl:w-1/2 lg:w-1/2 md:w-full",
        headerGridSize : "col-span-2 pl-2",
        card : "col-span-2 xl:col-span-1 lg:col-span-1 sm:col-span-2 md:col-span-2 p-2"
      }
    }
  },
  components: {
    CardHeader
      },
};
</script>

<style scoped>
.rainbow {
    text-align: center;
    text-decoration: underline;
    font-family: sans-serif;    
}
.rainbow_text_animated {
    background: linear-gradient(to right, #6666ff, #0099ff , #00ff00, #ff3399, #6666ff);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
    animation: rainbow_animation 6s ease-in-out infinite;
    background-size: 400% 100%;
}

@keyframes rainbow_animation {
    0%,100% {
        background-position: 0 0;
    }

    50% {
        background-position: 100% 0;
    }
}
</style>