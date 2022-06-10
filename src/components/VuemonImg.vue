<template>
  <div class="vuokemon-container">
    <img v-if="respuesta" class="fade-in" :src="obtenerImagen" />
    <img v-else class="fade-in hidden-vuokemon" :src="obtenerImagen" />
  </div>
</template>

<script>
export default {
  props: {
    vuemonId: {
      type: Number,
      required: true,
    },
    respuesta: {
      type: Boolean,
      default: false,
    },
  },
  data() {
    return {
      srcImg: "",
    };
  },
  computed: {
    // un getter computado
    obtenerImagen: function () {
      // `this` apunta a la instancia vm
      return `https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/dream-world/${this.vuemonId}.svg`;
    },
  },
};
</script>

<style scoped>
.vuokemon-container {
  height: 200px;
}

img {
  height: 200px;
  user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  -webkit-user-drag: none;
  -webkit-user-select: none;
}

.hidden-vuokemon {
  filter: brightness(0);
}
</style>