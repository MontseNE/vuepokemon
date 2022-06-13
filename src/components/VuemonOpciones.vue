<template>
  <div class="vuopciones-container">
    <ul>
      <li
        v-for="opcion in listaOpciones"
        :key="opcion.id"
        @click="$emit('respuesta', opcion.id)"
      >
        {{ opcion.name }}
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
  border: 3px solid #3329c0;
  cursor: pointer;
  margin-bottom: 0.8em;
  width: 250px;
  padding: 0.5em;
  color: #3329c0;
  font-weight: 600;
}

li:hover {
  background-color: rgba(0, 0, 0, 0.05);
}

.vuopciones-container {
  display: flex;
  justify-content: center;
}
</style>