<template>
  <section>
    qui ci vanno le card
  </section>
</template>

<script>

import axios from "axios"

export default {
  name: 'DischiList',
 components: {
    
  },
  data(){
    return{
        apiUrl:"https://flynn.boolean.careers/exercises/api/array/music",
        listaAlbum:[],
    }
  },

  created(){
    axios.get(this.apiUrl)
    .then((result)=>{
        this.listaAlbum = result.data;
        console.log(result);
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
section{
    height: calc(100vh - 5vh);
    background-color: #1e2d3b;
}
</style>
