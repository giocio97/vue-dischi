<template>

<div>
   <select v-model="inputGenere" @change="myEmit()" name="selection" id="genere" >
        <option value="all">all</option>
        <option value="Rock">Rock</option>
        <option value="Pop">Pop</option>
        <option value="Jazz">Jazz</option>
        <option value="Metal">Metal</option>

      </select> 
</div>
   



 
</template>

<script>



export default {
  name: 'SelectGenere',
   
  data(){
    return{
     inputGenere: "",

    }
    
  },
  methods:{
    myEmit(){
      this.$emit(`mySearch`, this.inputGenere);
      console.log(this.inputGenere);
    }
  }

   
    

  

 
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
