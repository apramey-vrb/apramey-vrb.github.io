<template>
  <div :class="classNames.grid">
    <div :class="classNames.headerGridSize">
        <h1 class="sm:text-3xl text-2xl font-medium title-font mb-2 text-gray-900">{{header}}</h1>
        <div class="h-1 w-20 bg-blue-500 rounded mb-6"></div>
      </div>
    <div v-for="ex in cards" v-bind:key="ex.id" :class="classNames.card">
        <Card :obj="ex"/>
    </div>
    </div>
</template>

<script>
import Card from "@/components/Card.vue"

export default {
  name: 'CardHeader',
  props: {
    cards: Array,
    header : String,
    classNames : Object
  },
  components:{
    Card
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
