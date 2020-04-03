<template>
  <div>
      <h1 v-on:click="changeHeader">{{header}}</h1>
  </div>
</template>
<script>

import { EventBus } from '@/eventBus'
export default {
  name: 'Test',
  props: {
    header:{
        type: String
    } 
  },
  methods: {
      changeHeader (){
          this.header = "changed header";
          EventBus.$emit('changeIt', 'changed header');
      }
  }
}
</script>