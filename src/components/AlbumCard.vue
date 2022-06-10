<template>
 <div class="card">
    <img :src="datails.poster" :alt="datails.title">
    <h4> {{datails.title}} </h4>
    <span> {{datails.author}} </span><br>
    <span> {{datails.year}} </span>
 </div>
 
</template>

<script>
export default {
   name: 'AlbumCard',
   props:{
    datails:Object
   } 
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
