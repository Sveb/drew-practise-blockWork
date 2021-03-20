<template lang="html">
  <div
    @mouseenter="cw()"
    @mouseover="isHovering = true"
    @mouseout="isHovering = false"
    :class="{ hoveredPanel: isHovering }"
    class="npPanel"
  >
    <h2>{{ title }}</h2>
    <span class="arrow">&#x2197;</span>
    <div class="breadcrumb">{{ text }}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isHovering: false
    };
  },
  props: {
    title: {
      type: String,
      default: "Next project"
    },
    text: {
      type: String,
      default: "CW"
    }
  }
};
</script>

<style lang="css" scoped>
@font-face {
  font-family: "zoom";
  src: url(../assets/fonts/zoom-pro-brutal-medium.woff);
}
.npPanel {
  font-family: zoom;
  font-size: 33px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  text-transform: uppercase;
  padding: 200px;
  position: relative;

  transition: 0.1s;
}

.npPanel h2 {
  display: inline;
  border-bottom: 3.5px solid black;
  transition: 0.1s;
  padding-bottom: 20px;
}
.npPanel span {
  font-family: calibri;
  font-size: 50px;
  padding: 15px;
  position: absolute;
  top: 226px;
  right: 150px;
  transition: 0.1s;
}

/* HOVER STATES */

.hoveredPanel {
  color: #fff335;
  background-image: url("../assets/images/rover.jpeg");
}
.hoveredPanel h2 {
  border-bottom: 3.5px solid #fff335;
}

.hoveredPanel span {
  color: #fff335;
}
.hoveredPanel .breadcrumb {
  opacity: 1;
}
.breadcrumb {
  opacity: 0;
  color: #fff335;

  transition: 0.1s;
}
</style>
