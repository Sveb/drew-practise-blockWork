<template>
  <blockwork
    title="Svebor"
    text="Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. "
    image="../assets/images/ballons.jpeg"
  />
</template>

<script>
import blockwork from "./components/blockwork.vue";

export default {
  name: "App",
  components: {
    blockwork
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
