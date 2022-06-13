<template>
 <div class="card">
   <div>
       <img :src="discoObjet.poster" :alt="discoObjet.title">
         <h4> {{discoObjet.title}} </h4>
       <span> {{discoObjet.author}} </span><br>
      <span> {{discoObjet.year}} </span>
   </div>
 </div>
 
</template>

<script>
export default {
   name: 'AlbumCard',
   props:{
    discoObjet:Object
   } 
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.card{
   
   flex-basis:calc(20% - 5px);
   text-align: center;
   
   background-color: #2e3a46;
   
   
   
    img{
      width: 160px;
     
      object-fit: contain;
      margin: 20px;
      
   }

   h4{
      color: white;
   }
   span{
      color: grey;
   }
   
  
   
}
</style>
