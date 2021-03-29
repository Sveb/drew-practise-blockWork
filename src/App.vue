<template>
  <NPpanel />
  <blockwork
    title="Svebor"
    text="Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. "
    image="../assets/images/ballons.jpeg"
  />
</template>

<script>
import blockwork from "./components/blockwork.vue";
import NPpanel from "./components/PanelNextPrevious.vue";
export default {
  name: "App",
  props: {
    image: {
      src: "../assets/images/jojo3.jpg"
    }
  },
  components: {
    blockwork,
    NPpanel
  }
};
</script>

<style>
#app {
  font-family: founders, Calibri, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
