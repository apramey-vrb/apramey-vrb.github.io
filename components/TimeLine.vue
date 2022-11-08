<template>
  <div class="opacity-100 mt-6">
    <ol class="relative border-l border-gray-200 dark:border-gray-700">
      <li class="mb-6 ml-6">
        <span
          class="flex absolute -left-3 justify-center items-center w-6 h-6 bg-blue-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-blue-900"
        >
          <img v-if="!isWork"
            class="w-3 h-3 text-blue-600 dark:text-blue-400"
            src="~assets/icon/academy.svg"
          />
          <img v-else
            class="w-3 h-3 text-blue-600 dark:text-blue-400"
            src="~assets/icon/work.svg"
          />
        </span>
        <h3
          class="flex items-center mb-1 text-lg font-semibold text-gray-900 dark:text-white"
        >
          <span v-html="title"></span>
          <!-- <span
            class="bg-blue-100 text-blue-800 text-sm font-medium mr-2 px-2.5 py-0.5 rounded dark:bg-blue-200 dark:text-blue-800 ml-3"
            >Currently</span
          > -->
        </h3>
        <time
          class="block mb-2 text-sm font-normal leading-none text-gray-400 dark:text-gray-500"
          >{{date}} &nbsp; | &nbsp; {{location}} </time
        >
        <p class="mb-4 text-base font-normal text-gray-500 dark:text-gray-400">
          <ul>
            <li v-for="(des) in description" v-bind:key="des" class="list-disc" v-html="des"></li>
          </ul>
        </p>
      </li>      
    </ol>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    date: String,
    location: String,
    description: Array,
    isWork : {
        type : Boolean,
        default : false
    }
  },
  data() {
    return {
      title: this.title,
      date: this.date,
      location: this.location,
      description: this.description,
      isWork: this.isWork
    };
  },
  methods: {
    formatDate(date) {
      const options = { year: "numeric", month: "long", day: "numeric" };
      return new Date(date).toLocaleDateString("en", options);
    },
  },
};
</script>

<style></style>
