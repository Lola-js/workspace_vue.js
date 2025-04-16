<template>
  <div class="app"> 
    <h1> Lista de mejores libros de los últimos 10 años</h1>
  
    <PostListE />
  </div> 
</template> 
  
<script>
  
  import PostListE from './components/PostListE.vue'
  
  export default {
    name:'App',
    components: {
      PostListE
    }    
  }
</script>
  
<style>
  #app{
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
  
</style>
  