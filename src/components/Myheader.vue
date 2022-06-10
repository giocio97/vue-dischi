<template>
 
 <header>
  <img src="../assets/img/spotify-brandlogo.net_.png" alt="logo">
 </header>
</template>

<script>
export default {
   name: 'MyHeader'  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
header{
background-color: #2e3a46;
height: 5vh;

img{
  width: 30px;
  height: 30px;
  object-fit: cover;
  margin: 5px;
}
}
</style>
