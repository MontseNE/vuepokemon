<template>
  <div class="vuopciones-container">
    <ul>
      <li v-for="opcion in listaOpciones" :key="opcion.id">
        {{ opcion.nombre }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    listaOpciones: {
      type: Array,
    },
  },
};
</script>

<style scoped>
ul {
  list-style-type: none;
}

li {
  background-color: white;
  border-radius: 8px;
  border: 2px solid rgba(0, 0, 0, 0.2);
  cursor: pointer;
  margin-bottom: 0.8em;
  width: 250px;
  padding: 0.5em;
}

li:hover {
  background-color: rgba(0, 0, 0, 0.05);
}

.vuopciones-container {
  display: flex;
  justify-content: center;
}
</style>