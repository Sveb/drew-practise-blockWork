<template lang="html">  this is for six-twenty-six
  <div @click="toggleMenu" class="hamburger">
    <div class="stLine">
    </div>
    <div class="ndLine">
    </div>

  </div>

</template>

<script>
export default {
  name: 'hamburger',
  props: {
    isOpened: {
      type: Boolean,
      default: false,
    }
  },
  methods: {
    toggleMenu() {
      this.$emit('toggle', !this.isOpened )
    }
  }
}
</script>

<style lang="css" scoped>
  .hamburger.stLine.ndLine {
    display: flex;
    flex-direction: column;

    transition: 0.4s;


  }
  .stLine{
    width: 30px;
    height: 2px;
    background-color: black;
    margin: 8px;

    transition: 0.4s;
  }
  .ndLine {
    width: 30px;
    height: 2px;
    background-color:black;
    margin: 8px;

    transition: 0.4s;
  }

  /* //Hover states */
 .hamburger:hover .stLine {
   transform: translateY(2px);
 }
 .hamburger:hover .ndLine {
   transform: translateY(-2px);
 }


</style>
