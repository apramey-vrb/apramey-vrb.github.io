<template>
  <div class="dark:bg-gray-900 mt-6">
    <div class="max-w-screen-lg md:flex mx-auto dark:bg-gray-900">
      <div class="md:w-1/3 p-2 md:flex md:justify-center">
        <AuthorCard />
      </div>
      <div class="md:w-2/3 px-8">
        <AuthorIntro></AuthorIntro>
        <!-- <Expertise></Expertise> -->
        <h4
        class="mt-6 text-2xl text-gray-700 font-bold capitalize dark:text-blue-200"
      >
        Present
        <div class="h-1 w-12 bg-blue-500 rounded mb-6"></div>
      </h4>
        <TimeLine class="ml-3" :title="present.title" :date="present.date" :location="present.location" :description="present.description" :isWork="present.isWork"></TimeLine>
        <h4
        class="mt-4 text-2xl text-gray-700 font-bold capitalize dark:text-blue-200"
      >
        Past
        <div class="h-1 w-12 bg-blue-500 rounded mb-6"></div>
      </h4>
      <TimeLine v-for="p in past" v-bind:key="p.title" class="ml-3" :title="p.title" :date="p.date" :location="p.location" :description="p.description" :isWork="p.isWork"></TimeLine>
      <h4
        class="mt-4 text-2xl text-gray-700 font-bold capitalize dark:text-blue-200"
      >
        Undergraduation
        <div class="h-1 w-12 bg-blue-500 rounded mb-6"></div>
      </h4>
      <TimeLine class="ml-3" :title="undergrad.title" :date="undergrad.date" :location="undergrad.location" :description="undergrad.description" :isWork="undergrad.isWork"></TimeLine>

      </div>
    </div>
  </div>
</template>

<script>
import siteMetaInfo from "@/data/sitemetainfo";
import {present, past, internships, undergrad} from "@/data/experience";
export default {
  data() {
    return {
      siteMetaInfo: siteMetaInfo,
      present: present,
      past: past,
      internships : internships,
      undergrad : undergrad
    };
  },
  head: {
    title: siteMetaInfo.title,
    meta: [
      { charset: "utf-8" },
      { name: "viewport", content: "width=device-width, initial-scale=1" },
      {
        hid: "description",
        name: "description",
        content: siteMetaInfo.description,
      },
    ],
    link: [{ rel: "icon", type: "image/x-icon", href: "/favicon.ico" }],
  },
};
</script>

<style></style>
