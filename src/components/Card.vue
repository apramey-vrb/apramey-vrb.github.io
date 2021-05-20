<template>
    <div class="flex flex-wrap -m-4">
    <div v-for="ex in obj" v-bind:key="ex.id" class="xl:w-1/4 md:w-1/2 p-4">
        <div  class="bg-gray-100  p-6 rounded-lg">
        <img class="h-40 pr-6 rounded w-full object-cover object-center" v-bind:src="ex.imgsrc" alt="content">
        <div class="">
            <h3 class="tracking-widest text-blue-500 text-xs font-medium title-font">{{ex.title}}</h3>
            <h2 class="text-lg text-gray-900 font-medium title-font mb-4">{{ex.subtitle}}</h2>
            <p class="leading-relaxed text-base">{{ex.description}}</p>
        </div>                
        </div>
    </div>           
    </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    obj: Object,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
