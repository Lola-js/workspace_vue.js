<template>
<!--boton color
--><button class="color-btn" @click="$emit ('cambiar-color')">
Cambiar de color</button>
</template>

<script>
export default {
  name: 'ColorButton'
}
</script>

<style scoped>

.color-btn{
    background-color: green;
    border: none;
    color: white;
    padding: 15px 32px;
    text-align: center;
    font-size: 16px;
    border-radius: 50px; 
    cursor: pointer;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    margin: 30px; 
    }

    
    .color-btn:hover {
      background-color: #7ba07d; 
      box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2); 
    }

   
</style>