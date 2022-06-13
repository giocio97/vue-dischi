<template>
 <div class="card">
    <img :src="discoObjet.poster" :alt="discoObjet.title">
    <h4> {{discoObjet.title}} </h4>
    <span> {{discoObjet.author}} </span><br>
    <span> {{discoObjet.year}} </span>
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

</style>
