<template>
  <header class="header" :style="{ backgroundImage: 'url(' + backgroundImg + ')' }">
    <div class="container">
      <navbar></navbar>
      <main-title>
      </main-title>
    </div>
  </header>
</template>


<style lang="scss">
@import "../assets/scss/variables.scss";
@import "../assets/scss/fonts.scss";
.header {
  background-color: $primaryColor;
  background-size: 1440px 100%;
  background-repeat: no-repeat;
  padding-top: 25px;
  padding-bottom: 100px;
  margin-bottom: 80px;
  @media (min-width: 1440px) {
    background-repeat: repeat-x;
  }
}
.heading__title {
  font-family: "Open Sans", Helvetica, sans-serif;
  font-size: 48px;
  text-align: center;
  margin: 0 auto;
  color: $white;
  margin-bottom: 85px;
  text-transform: uppercase;
}

.heading__text {
  @include bigText;
  text-align: center;
  padding: 0;
  margin: 0;
  color: $white;
}
</style>


<script>
import Navbar from "./Navbar";
import MainTitle from "./MainTitle";
export default {
  name: "TheHeader",
  components: {
    Navbar,
    MainTitle
  },
  data: function() {
    return {
      backgroundImg: "./static/img/background.jpg"
    };
  }
};
</script>

