<template>
  <a href class="worldwide__item">
    <img :src="partners.item.img" alt class="worldwide__img">
  </a>
</template>


<script>
export default {
  name: "WorldwideItem",
  props: {
    partners: {
      type: Object
    }
  }
};
</script>


<style lang="scss">
@import "../assets/scss/variables.scss";
.worldwide__item {
  display: block;
  margin-bottom: 50px;
}
</style>
