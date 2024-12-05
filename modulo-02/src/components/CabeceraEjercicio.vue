<template>
    <div class="cabecera-ejercicio">
      <!-- Slot por defecto (titulo para el ejercicio) -->
      <h1><slot></slot></h1>
      <!-- se pintaran en la app como se hayan nombrado aqui no como luego se pongan en la app-->
  
      <!-- Slot para la descripción del ejercicio,(app.vue=#descripcion)-->
      <p><slot name="descripcion"></slot></p>
    </div>
  </template>
  
  <script>
  import { defineComponent } from 'vue'; // defineComponent se usa en vez d setup para crear el componente y setup para la logica
   export default defineComponent({    
    name: 'CabeceraEjercicio',  
  });
  </script>
  
  <style scoped>
  .cabecera-ejercicio {
    background-color: #f4f4f4;
    padding: 20px;
    border-radius: 8px;
    margin-bottom: 20px;
    border: 1px solid #ccc;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }
  
  .cabecera-ejercicio h1 {
    font-size: 24px;
    color: #333;
    margin: 0;
  }
  
  .cabecera-ejercicio p {
    font-size: 16px;
    color: #666;
    margin-top: 10px;
  }
  </style>
  