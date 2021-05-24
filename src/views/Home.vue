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
              Yet another IT guy here!<br>
              Currently Software Engineer at First American<br>
              I love Technology, Photography, Travel and Philosophy </h3>
              <div class="flex mb-4">
                <div class="w-1/3  h-12 "><button class="bg-gray-200 hover:bg-blue-300 text-gray-800 font-semibold py-2 px-4  rounded shadow" onclick="window.location.href='https://twitter.com/ChhajedViraj';" >
                  Twitter
                </button></div>
                <div class="w-1/3  h-12 mx-3"><button class="bg-gray-200 hover:bg-blue-300 text-gray-800 font-semibold py-2 px-4  rounded shadow" onclick="window.location.href='https://www.linkedin.com/in/virajchhajed/';" >
                  LinkedIn
                </button></div>
                <div class="w-1/3  h-12"><button class="bg-gray-200 hover:bg-yellow-500 text-gray-800 font-semibold py-2 px-4  rounded shadow" onclick="window.location.href='https://www.instagram.com/viraj.chhajed/';" >
                  Instagram
                </button></div>
              </div>
          </div>
          <div class="lg:max-w-lg lg:w-full md:w-1/2 w-5/6">
          </div>
        </div>
      </section>


      <section class="text-gray-600 body-font">
        <div class=" container px-5 py-10 mx-auto">
          <div class="flex flex-wrap -mx-2 overflow-hidden sm:-mx-1 md:-mx-1 lg:-mx-3 xl:-mx-2">
              <CardHeader :cards="presentExperience" :header="'Present:'" :classNames="experienceClass" />
              <CardHeader :cards="pastExperience" :header="'Past:'" :classNames="experienceClass"/>
          </div>
        </div> 
      </section>

      <section class="text-gray-600 body-font">
        <div class=" container px-5 py-10 mx-auto">
          <CardHeader :cards="pastEducation" :header="'Education:'" :classNames="pastEducationClass" />
        </div> 
      </section>

      <section class="text-gray-600 body-font">
        <div class=" container px-5 py-10 mx-auto">
          <CardHeader :cards="skills" :header="'skills:'" :classNames="skillsClass" />
        </div> 
      </section>

      <section class="text-gray-600 body-font">
        <div class=" container px-5 py-10 mx-auto">
          <CardHeader :cards="projects" :header="'Projects:'" :classNames="projectClass" />
        </div> 
      </section>

      <section class="text-gray-600 body-font">
        <div class=" container px-5 py-10 mx-auto">
          <div class="flex flex-wrap">
            <div class="w-full sm:w-full md:w-full lg:w-1/2 xl:w-1/2 pl-6">
                <h1 class="sm:text-3xl text-2xl font-medium title-font mb-2 text-gray-900">Photography & Travel:</h1>
                <div class="h-1 w-20 bg-blue-500 rounded mb-6"></div>
            </div>
            <div class="self-center w-full sm:w-full md:w-full lg:w-1/2 xl:w-1/2 pl-6 mb-6">
            <h1 class="sm:text-base text-base font-medium title-font text-gray-900">Follow me on <a class="text-xl text-blue-500" href="">Twitter</a> & <a class="text-xl text-pink-500" href="">Instagram</a> for more content</h1>            
            </div>
          </div>
          <CardHeader :cards="photography" :isHtml="true" :classNames="photographyClass" />
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
          pointers : ["Awarded with Zoom Star and Zoom Miles Champion (2)🥇","Member of Core tech team👨‍💻","Worked, Designed and Delivered in core modules of INSZoom product like Case & KB, Forms, Questionnaires🚀","Actively participated in articulating coding standards and code review document📃","Conducted project training and knowledge sessions for new hires👶"],
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
        card : "col-span-2 xl:col-span-1 lg:col-span-1 sm:col-span-2 md:col-span-2 p-2",
        cardHoverColor : 'bg-gradient-to-r from-green-200 to-blue-200'
      },
      pastEducation : [
        {
          id : 5,
          title : "Bachelors of Engineering in Computer Science",
          subtitle : "SDM College of Engineering and Technology",
          date : "2014 - 2018 (Dharwad)",
          description : "Grade: 9.03",
          pointers : ["Google Facilitator (Applied CS with Android)","Internshala Student Partner","Actively participated in Techno-cultural fest : Insignia","Conducted many workshops and events."],
          imgsrc : ""
        },
        {
          id : 6,
          title : "Pre university",
          subtitle : "Royal Palace College",
          date : "2012 - 2014 (Jamkhandi)",
          description : "Grade : 97.5% (Physics & Mathematics : 100/100)",
          imgsrc : ""
        },
        {
          id : 6,
          title : "Grade 10",
          subtitle : "Parashuram Bahurao High School",
          date : "2012 (Jamkhandi)",
          description : "Grade : 92.5%",
          imgsrc : ""
        }
      ],
      pastEducationClass : {
        grid : "grid grid-cols-3 px-2 sm:w-full xl:w-full lg:w-full md:w-full",
        headerGridSize : "col-span-3 pl-2",
        card : "col-span-3 xl:col-span-1 lg:col-span-1 sm:col-span-2 md:col-span-2 p-2",
        cardHoverColor : 'bg-gradient-to-r from-pink-300 to-yellow-300'
      },
      projects : [
        {
          id : 8,
          title : "",
          subtitle : "Total Recording Solutions",
          date : "First American Title Corporation",
          description : "As a Software Engineer, I am responsible for creating different microservices and exposing valid API endpoints for the module I'm currently working on. Actively working on microservice architecture, serverless architecture and various AWS products to scale up and fasten up TRecS.",
          imgsrc : ""
        },
        {
          id : 8,
          title : "",
          subtitle : "Multiple Projects",
          date : "Inszoom",
          description : "As a Product Engineer, I built reusable web components, SPAs, and wrote backend logic from scratch. I was part of 'Core tech team' of Inszoom, where I conducted different POCs for different modules. I had exposure to all parts of SDLC cycle from requirement analysis to delievery.",
          imgsrc : ""
        },
        {
          id : 7,
          title : "Major Project",
          subtitle : "Smart Garbage Collector",
          date : "SDMCET Dharwad",
          description : "Collection of non-biodegradable and recyclable plastic waste through a robot with 3D-printed gripper coupled with an object detector built with deep learning framework 'Caffe', deployed on raspberry pi.",
          pointers : ["Grade: 10/10","Fully funded by ITBT Dept. Govt. of Karnataka.","Awarded as top 10 ITBT projects in Karnataka","Exhibited in 'Innovation Festival' at VITM, Bengaluru","Awarded as 'Top 3000 start-up innovations' by IIM Calcutta and quenched prize worth of $2280"],
          imgsrc : ""
        },
        {
          id : 8,
          title : "Minor Project",
          subtitle : "Study of Image Textural Features of Human Brain with Abnormality Analysis",
          date : "SDMCET Dharwad",
          description : "A system to detect abnormalities in human brain MRI scans using textural properties and intensity variations of healthy and unhealthy brain MRI scans. (Grade : 10/10)",
          imgsrc : ""
        },
        
      ],
      projectClass : {
        grid : "grid grid-cols-4 px-2 sm:w-full xl:w-full lg:w-full md:w-full",
        headerGridSize : "col-span-4 pl-2",
        card : "col-span-4 xl:col-span-1 lg:col-span-1 sm:col-span-2 md:col-span-2 p-2",
        cardHoverColor : 'bg-gradient-to-r from-pink-300 to-yellow-300'
      },
      photography : [
        {
          id : 1212,
          htmlContent : "<blockquote class=\"twitter-tweet\" data-conversation=\"none\" data-lang=\"en\" data-dnt=\"true\" data-theme=\"dark\"><p lang=\"und\" dir=\"ltr\"><a href=\"https://t.co/9QwT9TrbZS\">pic.twitter.com/9QwT9TrbZS</a></p>&mdash; Apramey Bhat (@apramey8) <a href=\"https://twitter.com/apramey8/status/1396829981997559817?ref_src=twsrc%5Etfw\">May 24, 2021</a></blockquote> "
        },
        {
          id : 121,
          htmlContent : "<blockquote class=\"twitter-tweet\" data-conversation=\"none\" data-dnt=\"true\" data-theme=\"dark\"><p lang=\"und\" dir=\"ltr\"><a href=\"https://t.co/441Wp9Ykz3\">pic.twitter.com/441Wp9Ykz3</a></p>&mdash; Apramey Bhat (@apramey8) <a href=\"https://twitter.com/apramey8/status/1396829967543984131?ref_src=twsrc%5Etfw\">May 24, 2021</a></blockquote>"
        },
        {
          id : 122,
          htmlContent : "<blockquote class=\"twitter-tweet\" data-conversation=\"none\" data-lang=\"en\" data-dnt=\"true\" data-theme=\"dark\"><p lang=\"und\" dir=\"ltr\"><a href=\"https://t.co/0WikVY0AqQ\">pic.twitter.com/0WikVY0AqQ</a></p>&mdash; Apramey Bhat (@apramey8) <a href=\"https://twitter.com/apramey8/status/1396829974984757255?ref_src=twsrc%5Etfw\">May 24, 2021</a></blockquote>"
        },
        {
          id : 123,
          htmlContent : "<blockquote class=\"twitter-tweet\" data-conversation=\"none\" data-dnt=\"true\" data-theme=\"dark\"><p lang=\"und\" dir=\"ltr\"><a href=\"https://t.co/rsAksAbbTH\">pic.twitter.com/rsAksAbbTH</a></p>&mdash; Apramey Bhat (@apramey8) <a href=\"https://twitter.com/apramey8/status/1396847350933450752?ref_src=twsrc%5Etfw\">May 24, 2021</a></blockquote>"
        }
      ],
      photographyClass : {
        grid : "grid grid-cols-4 px-2 sm:w-full xl:w-full lg:w-full md:w-full",
        headerGridSize : "col-span-4 pl-2",
        card : "col-span-4 xl:col-span-1 lg:col-span-1 sm:col-span-2 md:col-span-2 p-2",
        cardHoverColor : 'bg-gradient-to-r from-pink-300 to-yellow-300'
      },
      skills : [
        {
          subtitle : "C#",
          imgsrc : ""
        },
        {
          subtitle : "Vue",
          imgsrc : ""
        },
        {
          subtitle : "Javascript",
          imgsrc : ""
        },
        {
          subtitle : ".Net Core",
          imgsrc : ""
        },{
          subtitle : "MSSQL",
          imgsrc : ""
        },{
          subtitle : "Dapper",
          imgsrc : ""
        },{
          subtitle : "Git",
          imgsrc : ""
        },{
          subtitle : "Azure",
          imgsrc : ""
        },{
          subtitle : "AWS",
          imgsrc : ""
        }
        
        
      ],
      skillsClass : {
        grid : "grid grid-cols-8 px-2 sm:w-full xl:w-full lg:w-full md:w-full",
        headerGridSize : "col-span-8 pl-2",
        card : "col-span-3 xl:col-span-1 lg:col-span-1 sm:col-span-3 md:col-span-3 p-2",
        cardHoverColor : 'bg-gradient-to-r from-green-200 to-blue-200'
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
    animation: rainbow_animation 10s ease-in-out infinite;
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