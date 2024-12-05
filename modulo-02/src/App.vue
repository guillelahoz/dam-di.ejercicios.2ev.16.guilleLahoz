<template>
  <div>
    <CabeceraEjercicio>
      <!-- (slot por defecto==<slot></slot>,en cabeceraEjercicio) -->
      Ejercicio-1

      <!-- Descripción del ejercicio 1 (slot con nombre 'descripcion') -->
      <template #descripcion>
      Incluye Descripción
      </template>
    </CabeceraEjercicio>

    <CabeceraEjercicio>
      <!-- Título del ejercicio 2 (slot por defecto) -->
      Ejercicio-2

      <!-- Descripción del ejercicio 2 (igual que el 1) -->
      <template #descripcion>
      Eventos de ciclo de vida   <!-- los template son para los slots solo-->
      </template>     
  
      <Ej02 />
          
    </CabeceraEjercicio>
  </div>
</template>

<script>
import CabeceraEjercicio from './components/CabeceraEjercicio.vue';
import Ej02 from './components/Ej02.vue';



export default {
  components: {
    CabeceraEjercicio,
    Ej02,
  }
};


</script>
