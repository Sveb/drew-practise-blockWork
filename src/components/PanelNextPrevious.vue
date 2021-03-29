<template lang="html">
  <div
    @mouseover="isHovering = true"
    @mouseout="isHovering = false"
    :class="{ hoveredPanel: isHovering }"
    class="npPanel"
  >
    <img
      class="demo-bg"
      src="../assets/images/jojo2.png"
      alt=""
      style="max-height: 700px;"
    />
    <div class="titelArrowContainer">
      <a href="#">
        <h2>{{ title }}</h2>
        <span class="span1">&#x2197;</span>
        <span class="span2">&#8594;</span>
      </a>
    </div>
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

/* .background-image-opacity-0 {
  background-image: url("../assets/images/rover.jpeg");
} */
a {
  text-decoration: none;
  color: inherit;
}
.npPanel {
  position: relative;
  font-family: zoom;
  font-size: 33px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  text-transform: uppercase;
  width: 50%;
  height: auto;
  margin-bottom: 400px;
  padding: 200px;
}

.npPanel h2 {
  display: inline;
  border-bottom: 3.5px solid black;
  transition: 0.2s;
  padding-bottom: 20px;
}
.npPanel .span1 {
  font-family: calibri;
  font-size: 50px;
  padding: 15px;
  position: absolute;
  bottom: -17px;
  transition: 0.2s;
}
.npPanel .span2 {
  font-family: calibri;
  font-size: 50px;
  transition: 0.2s;
  position: absolute;
  opacity: 0;
}

.demo-bg {
  opacity: 0;
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: auto;
  transition: 0.2s;
}

.breadcrumb {
  opacity: 0;
  color: #fff335;
  transition: 0.2s;
  padding-top: 50px;
  font-family: founders;
  font-size: 62px;
}

.titelArrowContainer {
  position: relative;
}

/* HOVER STATES */

.hoveredPanel {
  color: #fff335;
}
.hoveredPanel .demo-bg {
  opacity: 1;
}
.hoveredPanel h2 {
  border-bottom: 3.5px solid #fff335;
}

.hoveredPanel .span1 {
  color: #fff335;
}
.hoveredPanel .breadcrumb {
  opacity: 1;
  z-index: 1;
}

/* BREAKPOINTS */

@media (max-width: 1559px) {
  .npPanel {
    padding-bottom: 100px;
  }
  .npPanel h2 {
    border-bottom: none;
    display: flex;
    text-align: center;
    border-bottom: 3.5px solid black;
  }
  .titelArrowContainer {
    display: flex;
    justify-content: center;
  }

  .npPanel .span1 {
    opacity: 0;
  }
  .npPanel .span2 {
    opacity: 1;
    align-self: flex-end;
    position: absolute;
    bottom: -30px;
  }

  .hoveredPanel .breadcrumb {
    opacity: 0;
  }
  .hoveredPanel h2 {
    border-bottom: 3.5px solid #fff335;
  }
}
</style>
