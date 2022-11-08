<template>
  <div class="md:fixed">
    <div class="md:block flex justify-center items-center">
      <nuxt-img
        :src="siteMetadata.author_image"
        loading="lazy"
        alt="me"
        class="shadow-xl md:h-60 md:w-60 h-40 w-40 rounded-full"
      />
      <div class="mb-2 mx-7 mt-4 justify-center items-center">
        <h1
          class="md:text-3xl text-2xl text-gray-800 font-bold dark:text-blue-100"
        >
          {{ siteMetadata.author }}
      </h1>
      </div>
    </div>

    <TheFooter/>

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
