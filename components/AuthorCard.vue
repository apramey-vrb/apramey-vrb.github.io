<template>
  <div class="md:fixed">
    <div class="md:block flex justify-center items-center">
      <div class="content-center">
        <nuxt-img
        :src="siteMetadata.author_image"
        loading="lazy"
        alt="me"
        class="shadow-xl rounded-full object-center h-64 w-64 md:h-60 w-60"
      />
      </div>
     
     
    </div>
    <div class="mb-2 mx-7 mt-4 justify-center items-center">
      <h1
        class="md:text-3xl text-2xl text-center text-gray-800 font-bold dark:text-blue-100"
      >
        {{ siteMetadata.author }}
    </h1>
    <div class="items-center">
    <p class="mt-3 text-center">📍 Helsinki, Finland</p>
    <p class="text-center"><a href="mailto:hello@apra.me">📧 hello [at] apra.me</a></p>
  </div>
    </div>
    <TheFooter/>

    <div class="grid content-center grid-cols-1 gap-4" style="display:flex; justify-content:center;">
    <button class="bg-blue-500 hover:bg-blue-700 w-40 h-10 text-white font-bold py-2 px-4 rounded inline-flex items-center">
      <svg class="fill-current w-4 h-4 mr-2" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M13 8V2H7v6H2l8 8 8-8h-5zM0 18h20v2H0v-2z"/></svg>
      <a href="/AprameyBhat_CV_SECCLO.pdf" target="_blank" download="">Download CV</a>
    </button>
  </div>
  </div>
</template>

<script>
import Mail from "../assets/icon/mail.svg?inline";
import Github from "../assets/icon/github_new.svg?inline";
import Globe from "../assets/icon/glob.svg?inline";
import siteMetaInfo from "@/data/sitemetainfo";
import TheFooter from "../components/TheFooter.vue";
export default {
  components: { Mail, Github, Globe },
  data: () => {
    return {
      siteMetadata: siteMetaInfo,
    };
  },
};
</script>
