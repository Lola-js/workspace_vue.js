<template>
    <div class="post">
      <h3>{{ title }}</h3>
      <h4>{{ autor }}</h4>
      <p>{{ description }}</p>
      <img :src="imagen" alt="imagen del libro" />
    </div>
  </template>
  
  <script>
  export default {
    name: 'PostDetail',
    props: {
      title: String,
      autor: String,
      description: {
        type: String,
        default: 'Descripción no disponible'
      },
      imagen: {
        type: String,
        default: ''
      }
    }
  }
  </script>
  
  <style scoped>
  .post {
    width: 250px;
    border: 1px solid #ccc;
    border-radius: 8px;
    padding: 1rem;
    background-color: #f4f4f4;
  }
  .post img {
    width: 100%;
    height: auto;
    border-radius: 4px;
  }
  </style>
  