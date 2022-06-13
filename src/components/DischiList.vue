<template>
<main>

  <SelectGenere @mySearch = "searchGenere"/>

       <section>
     
    <AlbumCard
    v-for="(item, index) in filteredGenere"
    :key="index"
    :discoObjet="item"
    />
  </section>
</main>

 
</template>

<script>

import axios from "axios"
import AlbumCard from '@/components/AlbumCard.vue'
import SelectGenere from "./SelectGenere.vue";

export default {
  name: 'DischiList',
   components: {
    AlbumCard,
    SelectGenere
},
  data(){
    return{
        apiUrl:"https://flynn.boolean.careers/exercises/api/array/music",
        listaAlbum: [],
        userText: "",
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
    },

    searchGenere(genereUser){
      this.userText = genereUser;
    }
  },
  computed:{
    filteredGenere(){
      if (this.userText === ""){
      return this.listaAlbum;
      } else{
        return this.listaAlbum.filter(item => {
        return item.genre.toLowerCase().includes(this.userText.toLowerCase());
        
      });
      }
    },
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
main{
  background-color: #1e2d3b;
  text-align: center;
   height: calc(100vh - 5vh);
  section{
   
    
    display: flex;
   justify-content: center;
   justify-items: flex-start;
    flex-wrap: wrap;
    padding: 30px;
    gap: 5px;
     
}
}
</style>
