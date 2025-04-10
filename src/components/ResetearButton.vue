<template>
  <!-- boton resetear-->
    <button class="color-resetear" @click="$emit ('resetear-color')">
        Resetear el color
    </button>        
</template>

<script>
export default {
  name: 'ResetearButton'
}

</script>

<style scoped>
 .color-resetear{
    background-color: rgb(26, 26, 248);
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

    
    .color-resetear:hover {
      background-color: #7ba07d; 
      box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2); 
    }

</style>