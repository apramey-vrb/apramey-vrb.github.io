<template>
<div class="flex flex-wrap w-full mb-6"> 
    <div v-for="item in items" v-bind:key="item.id" class="lg:w-1/2 w-full mb-2 pl-6 lg:mb-0">
        <h1 class="sm:text-3xl text-2xl font-medium title-font mb-2 text-gray-900">{{item}}</h1>
        <div class="h-1 w-20 bg-blue-500 rounded"></div>
    </div>
</div>
</template>

<script>
export default {
  name: 'CardHeader',
  props: {
    items: Array,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
