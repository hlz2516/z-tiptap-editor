<template>
  <div id="app">
   <Tiptap v-model="content" />
  </div>
</template>

<script>
import Tiptap from './components/Tiptap.vue';
export default {
  name: 'App',
  components: {
    Tiptap
  },
  data() {
    return {
      content:'',
      testOptions:{
        method:'output',
        eachParams:[
          
        ]
      }
    }
  },
  methods:{
    output(content){
      console.log(content);
    },
    setTextColor(event,color){
      event.target.style.setProperty('color',color)
    }
  }
}
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  width: 800px;
  height: 300px;
}


</style>
