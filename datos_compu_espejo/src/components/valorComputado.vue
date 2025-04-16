<template>
    <div class="caja">
      <h2> Espejo mágico</h2>
      <input type="text" v-model="message" placeholder="Escribe algo" />
      <p><b>Lo que estás escribiendo: </b>{{ message }}</p>
      <p><b>Mensaje en reversa:</b> {{ reversedMessage }}</p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'valorComputado',
    data() {
      return {
        message: ''
      };
    },
    computed: {
      reversedMessage() {
        return this.message.split('').reverse().join('');
      }
    }
  };
  </script>
  
  <style scoped>
  input {
    padding: 0.5rem;
    margin-top: 1rem;
    border: 1px solid #ccc;
    border-radius: 8px;
  }
  .caja{
  
  width: 300px;
  height: 300px;
  margin: 20px auto;
  padding: 10px;
  border-radius: 20px;
  background: linear-gradient(145deg, #d9d9d9, #ffffff);
  border: 2px solid rgba(255, 255, 255, 0.5);
  backdrop-filter: blur(6px);
  color: #333;
  font-family: 'Segoe UI', sans-serif;
  text-align: center;
  transition: transform 0.4s ease, box-shadow 0.4s ease;
}

.caja:hover {
  transform: scale(1.05);
  box-shadow:
    inset 0 0 30px rgba(255, 255, 255, 0.7),
    inset 0 0 60px rgba(255, 255, 255, 0.4),
    0 15px 40px rgba(0, 0, 0, 0.3);
}

  
  </style>
  