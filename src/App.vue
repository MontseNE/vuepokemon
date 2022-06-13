<template>
  <img src="./assets/pregunta.png" alt="" />
  <VuemonPage />
</template>

<script>
import VuemonPage from "./pages/VuemonPage.vue";

export default {
  name: "App",
  components: {
    VuemonPage,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #18314a;
  margin-top: 60px;
}
</style>
