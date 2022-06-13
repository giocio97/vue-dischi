<template>
  <section>
  <AlbumCard
    v-for="item in listaAlbum"
    :key="item"
    :discoObjet="item"
  />
  </section>
</template>

<script>

import axios from "axios"
import AlbumCard from './components/AlbumCard.vue'

export default {
  name: 'DischiList',
   components: {
            AlbumCard,
  },
  data(){
    return{
        apiUrl:"https://flynn.boolean.careers/exercises/api/array/music",
        listaAlbum: []
    }
  },

  created(){
    this.getAlbum();
  },

  methods:{
    getAlbum(){
        axios
        .get(this.apiUrl)
        .then((result) => {
        this.listaAlbum = result.data.response;
        console.log(result);
    })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
section{
    height: calc(100vh - 5vh);
    background-color: #1e2d3b;
    display: flex;
    justify-content: space-between;
}
</style>
