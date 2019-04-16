<template>
  <a href class="more-button">View All Our Products</a>
</template>


<style lang="scss">
@import "../assets/scss/variables.scss";
@import "../assets/scss/fonts.scss";
.more-button {
  @include smallText;
  display: block;
  margin: 0 auto;
  width: 230px;
  padding: 18px 45px;
  color: #000;
  border: 1px solid $accientColor;
  border-radius: 4px;
  text-align: center;
}
</style>


<script>
export default {
  name: "LoadButton"
};
</script>