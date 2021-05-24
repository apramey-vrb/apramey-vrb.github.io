<template>
  <div :class="classNames.grid">
    <div v-if="header && header != ''" :class="classNames.headerGridSize">
        <h1 class="sm:text-3xl text-2xl font-medium title-font mb-2 text-gray-900" v-html="header"></h1>
        <div class="h-1 w-20 bg-blue-500 rounded mb-6"></div>
      </div>
    <div v-for="ex in cards" v-bind:key="ex.id" :class="classNames.card" class="max-h-full">
        <Card :obj="ex" :isHtml="isHtml" :cardHoverColor="classNames.cardHoverColor"/>
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
    classNames : Object,
    isHtml : Boolean
  },
  components:{
    Card
  }
};
</script>