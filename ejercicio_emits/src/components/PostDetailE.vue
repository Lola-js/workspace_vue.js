<template>
    <div class="post">
      <h3>{{ title }}</h3>
      <h4>{{ autor }}</h4>
      <p>{{ description }}</p>
      <button class="btn" @click="hacerClick">Posición en el ranking</button>
      <br><br><br>
      <img :src="imagen" alt="imagen del libro" />
       
    </div>
  </template>
  
  <script>
  export default {
    name: 'PostDetailE',
    props: {
      title: {
        type:String,
      },
      autor: {
        type:String,
      },
      description: {
        type: String,
        default: 'Descripción no disponible'
      },
      imagen: {
        type: String,
        default: ''
      },
      mensaje:{
        type:String,
      }
    },
    emits: ["ranking" ],

    setup(props, {emit}){
        const hacerClick=()=>{
            emit("ranking",props.mensaje)
        }
        return { hacerClick }
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
  .btn{
    padding: 10px 20px;
    background-color: #2e9dcc;
    color: white;
    border-radius: 12px;
    font-size: 16px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    cursor: pointer;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }

  .btn:hover{
    transform: translateY(-2px);
    box-shadow: 0 6px 12px rgba(0,0,0,0.3);
  }
  </style>
  