<template>
  <div id="app">
   
    <MyHeader/>
    
    <DischiList/>
  </div>
</template>

<script>

import MyHeader from './components/Myheader.vue'
import DischiList from './components/DischiList.vue'

export default {
  name: 'App',
  components: {
   MyHeader,
   DischiList,
   
  }
}
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  
  color: #2c3e50;
  
}
</style>
