<template>
    <div>
      <!-- Botón que cambia el valor de 'disparador' -->
      <button @click="disparar">
        DISPARAR - {{ disparador }} 
      </button>
  
      <!-- Mostrar el contenido de debug -->
      <ul>
        <li v-for="(message, index) in debug" :key="index">
          {{ index }}: {{ message }}
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  import { ref, onMounted, onUnmounted, onBeforeUpdate } from 'vue';
  
  export default {
    name: 'Ej02',
    setup() {
      // Variables reactivas
      const disparador = ref('disparar');  // variable que toma como valor inicial disparar
      const debug = ref([]);               // array reactivo 'debug'
  
      // Función para cambiar el valor de 'disparador' al valor de Date.now()
      const disparar = () => {
        disparador.value = Date.now();   // actualiza el valor de disparador mediante el click del boton
      };
  
      // Evento 'onMounted' (cuando el componente se monta)
      onMounted(() => {
        debug.value.push('onMounted: El componente se ha montado.');
      });
  
      // Evento 'onBeforeUpdate' (cuando el componente está por actualizarse)
      onBeforeUpdate(() => {
        debug.value.push('onBeforeUpdate: El componente va a actualizarse.');
      });
  
      // Evento 'onUnmounted' (cuando el componente se desmonta)
      onUnmounted(() => {
        debug.value.push('onUnmounted: El componente se ha desmontado.');
      });
  
      // Devolver las variables y funciones reactivas
      return {
        disparador,
        debug,
        disparar
      };
    }
  };
  </script>
  
  <style scoped>
  button {
    padding: 10px 20px;
    font-size: 16px;
    background-color: #4CAF50;
    color: white;
    border: none;
    cursor: pointer;
    margin-bottom: 20px;
  }
  
  button:hover {
    background-color: #45a049;
  }
  
  ul {
    list-style-type: none;
    padding-left: 0;
  }
  
  li {
    font-size: 14px;
    color: #555;
  }
  </style>
  