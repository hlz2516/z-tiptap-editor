<template>
  <div id="app">
    
    <div class="box1">
      <div></div>
      <!-- <tiptap v-model="content" /> -->
      <div>
        <tiptap v-model="content" />
      </div>
    </div>
    <div></div>
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
  width: 1200px;
  height: 600px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: stretch;
}

#app>div{
  flex: 1;
}

.box1{
  display: flex;
  flex-direction: row;
  flex-flow: nowrap;
}

.box1>div{
  flex: 1;
}
</style>
