<template>
  <div> <h1>{{header}}</h1></div>
</template>
<script>
import { EventBus } from '@/eventBus';
export default {
  name: 'Test2',
  data(){
      return{
          header:"Something"
      }    
  },
  created(){
    EventBus.$on('changeIt', (data) => {
      this.header = data;
    })
  }
}
</script>