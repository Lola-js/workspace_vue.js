<template>
    <div class="color-card" :style="{ backgroundColor: color }">
        <h2>Pulsa un botón para cambiar el color</h2>
        <ColorBoton @cambiar-color="cambiarColor" />
        <ResetearBoton @resetear-color="resetearColor" />
      </div>
    </template>
    
    <script>
        //importar el componente boton color+resetear
        import ColorBoton from './colorBoton.vue';
        import ResetearBoton from './ResetearBoton.vue';
    
        export default {
      components: {
        ColorBoton,
        ResetearBoton
      },
      data() {
        return {
          color: 'gray'  
        }
      },
      methods: {
        cambiarColor() {
          if (this.color === 'gray') {
            this.color = 'red'
          } else if (this.color === 'red') {
            this.color = 'blue'
          } else if (this.color== 'blue'){
            this.color = 'yellow'
          } else if (this.color== 'yellow'){
            this.color = 'orange'
          }else{
            this.color = 'gray'
          }
        },
          resetearColor() {
          this.color = 'gray'
        }
      }
      }
    </script>
    
    <style>
    .color-card{
        background-color: rgb(180, 176, 176);
        margin: 30px;
        width: 300px;
        height: 300px;
        display:flex;
        flex-direction: column;
        align-items: center;
        justify-content: flex-start;
        padding:20px;
    }
    
    .botones_contenedor{
      display: flex;
      gap: 20px; 
      justify-content: center;  
      margin-top: 25px;
    }
    
    </style>