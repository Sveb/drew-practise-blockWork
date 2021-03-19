<template lang="html">
  <div class="container">
    <div class="card">
      <div class="image-container">
        <img src="../assets/images/ballons.jpeg" alt="" />
      </div>

      <div class="text-container">
        <h1>{{ title }}</h1>
        <p>{{ text }}</p>
      </div>
    </div>
    <div class="card">
      <div class="image-container">
        <img src="../assets/images/jojo.jpg" alt="" />
      </div>
      <div class="text-container">
        <h1>{{ title }}</h1>
        <p>{{ text }}</p>
      </div>
    </div>
    <div class="card">
      <div class="image-container">
        <img src="../assets/images/city.jpeg" alt="" />
      </div>
      <div class="text-container">
        <h1>{{ title }}</h1>
        <p>{{ text }}</p>
      </div>
    </div>
    <div class="card">
      <div class="image-container">
        <img src="../assets/images/angel.jpg" alt="" />
      </div>
      <div class="text-container">
        <h1>{{ title }}</h1>
        <p>{{ text }}</p>
      </div>
    </div>
    <div class="card">
      <div class="image-container">
        <img src="../assets/images/jojo2.png" alt="" />
      </div>
      <div class="text-container">
        <h1>{{ title }}</h1>
        <p>{{ text }}</p>
      </div>
    </div>
    <div class="card">
      <div class="image-container">
        <img src="../assets/images/jojo3.jpg" alt="" />
      </div>
      <div class="text-container">
        <h1>{{ title }}</h1>
        <p>{{ text }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    image: {
      // Mock: api.page
      type: Object,
      default: () => {}
    },
    isFullWidth: {
      type: Boolean,
      default: true
    },
    to: {
      type: String,
      default: ""
    },
    title: {
      type: String,
      default: ""
    },
    text: {
      type: String,
      default: ""
    }
  }
};
</script>

<style lang="css" scoped>
/* // fonts // */

@font-face {
  font-family: "cirka";
  src: url(../assets/fonts/cirka-regular.woff);
}
@font-face {
  font-family: "founders";
  src: url(../assets/fonts/founders-grotesk-light.woff);
}

.container {
  background-color: #fccc2e;
  width: 100%;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}

.card {
  height: auto;
  width: 47%;
  margin: 49px 30px 150px 30px;
  box-sizing: content-box;
  overflow: hidden;
}

.image-container {
  transition: 0.3s ease-out;
}

.image-container img {
  width: 100%;
  height: auto;
}

.card:nth-of-type(5) {
  width: 95%;
  margin: auto;
}

.text-container {
  margin-top: 0;
  margin-left: 20px;
  padding: 10px;
}

.text-container h1 {
  font-family: cirka;
  margin-top: 0;
  margin-bottom: 15px;
  font-size: 50px;
  padding: 0;
}

.text-container p {
  font-size: 26px;
  font-family: founders;
  margin-top: 0;
}

/* HOVER STATE */

.card:hover .image-container {
  transform: scale(1.05);
}

/* BREAK POINT */

@media (max-width: 1364px) {
  .container {
    flex-direction: column;
  }
}
</style>
