<template>
  <h1>¿Qué Vuemon es?</h1>
  <VuemonImg :vuemon-id="500" :respuesta="true" />
  <VuemonOpciones
    :lista-opciones="[
      { id: 25, nombre: 'miNombre' },
      { id: 526, nombre: 'tuNombre' },
      { id: 432, nombre: 'elNombre' },
      { id: 587, nombre: 'suNombre' },
    ]"
  />
</template>

<script>
import VuemonOpciones from "@/components/VuemonOpciones.vue";
import VuemonImg from "@/components/VuemonImg.vue";
export default {
  components: {
    VuemonOpciones,
    VuemonImg,
  },
};
</script>

<style>
</style>