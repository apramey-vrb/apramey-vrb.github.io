<template>
        <div @mouseover="active = false" @mouseleave="active = true" v-bind:class="active ? 'bg-gray-100' : cardHoverColor" class="p-6 rounded-lg">
                
            <div v-if="(!isHtml) && (active || !obj.pointers)">
                <img v-if="obj.imgsrc && obj.imgsrc != ''" class="h-40 pr-6 rounded w-full object-cover object-center" v-bind:src="obj.imgsrc" alt="content">
                <h3 class="tracking-widest text-blue-500 text-xs font-medium title-font">{{obj.title}}</h3>
                <h2 class="text-lg text-gray-900 font-medium title-font">{{obj.subtitle}}</h2>
                <h5 class="text-xs text-blue-500 mb-4">{{obj.date}}</h5>
                <p class="leading-relaxed text-base" v-html="obj.description"></p>
            </div>
            <div v-else-if="obj.pointers && obj.pointers.length > 0">
                <ul class="list-inside list-disc">
                    <li v-for="point in obj.pointers" v-bind:key="point.id" v-html="point" class="font-semibold">
                </li>
                </ul>
            </div>
            <div v-else-if="isHtml">
                <span v-html="obj.htmlContent"></span>
            </div>
        </div>

</template>

<script>
export default {
  name: 'Card',
  props: {
    obj: Object,
    cardHoverColor : String,
    isHtml : {
        type : Boolean,
        default : false
    }
  },
  data() {
      return {
          active : true,
          classActive : true
      }
  },
  methods:{
      
  }
};
</script>

<style scoped>
</style>
