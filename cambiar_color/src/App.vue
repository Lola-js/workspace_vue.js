<template>
  <h1>Lista de cartas</h1>
  <PostalContenedor />

  <ContadorOption />

  <ColorPostal />
</template>

<script setup>
  import PostalContenedor from './components/PostalContenedor.vue'
  import ContadorOption from './components/ContadorOption.vue'
  import ColorPostal from './components/ColorPostal.vue'
</script>

<style>
h1{
  
  color:blue;
}
</style>
