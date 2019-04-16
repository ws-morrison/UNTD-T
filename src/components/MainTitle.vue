<template>
  <div class="main-title">
    <h1 class="main-title__title">
      We solve
      <br>your problems
    </h1>
    <p class="main-title__text">{{leadText}}</p>
  </div>
</template>

<style lang="scss">
@import "../assets/scss/variables.scss";
@import "../assets/scss/fonts.scss";
.main-title {
  &__title {
    @include mainTitle;
    text-align: center;
    margin: 0 auto;
    color: $white;
    margin-bottom: 85px;
    text-transform: uppercase;
  }
  &__text {
    @include bigText;
    text-align: center;
    padding: 0;
    margin: 0;
    color: $white;
  }
}
</style>


<script>
export default {
  name: "MainTitle",

  data() {
    return {
      leadText:
        "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Fuga minima odit nesciunt ad totam non molestias recusandae unde velit! Nemo aspernatur non aliquid eius nostrum repudiandae. Voluptatum in nobis unde."
    };
  }
};
</script>
