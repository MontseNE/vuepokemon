<template>
  <div v-if="vuemonId">
    <VuemonImg :vuemon-id="vuemonId" :respuesta="hayRespuesta" />
    <VuemonOpciones
      @respuesta="activarRespuesta"
      :lista-opciones="listaOpciones"
    />
  </div>
  {{ msg }}
</template>

<script>
import getPokemonOptions from "@/helpers/vuokemonUtilidades";
import VuemonOpciones from "@/components/VuemonOpciones.vue";
import VuemonImg from "@/components/VuemonImg.vue";
export default {
  data() {
    return {
      vuemonId: null,
      hayRespuesta: false,
      msg: "",
      listaOpciones: [],
    };
  },

  components: {
    VuemonOpciones,
    VuemonImg,
  },

  methods: {
    activarRespuesta(dato) {
      this.hayRespuesta = true;
      if (dato == this.vuemonId) {
        this.msg = "Felicidades has acertado!!!!";
      } else {
        this.msg = "Eres un petardo!!";
      }
    },
    async cargar() {
      this.listaOpciones = await getPokemonOptions();

      this.vuemonId =
        this.listaOpciones[Math.floor(Math.random() * (4 - 0)) + 0].id;
    },
  },

  mounted() {
    this.cargar();
  },
};
</script>

<style>
</style>