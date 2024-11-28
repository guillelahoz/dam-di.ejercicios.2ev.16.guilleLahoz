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
        Uso de componente con slots con informacion estatica
      </template>
    </CabeceraEjercicio>
  </div>
</template>

<script>
import CabeceraEjercicio from './components/CabeceraEjercicio.vue';

export default {
  components: {
    CabeceraEjercicio
  }
};
</script>
