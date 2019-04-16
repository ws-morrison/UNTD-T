<template>
  <li class="additional__item">
    <a :href="additionalStorage.item.url" class="additional__link">{{additionalStorage.item.name}}</a>
  </li>
</template>


<style lang="scss">
@import "../assets/scss/variables.scss";
@import "../assets/scss/fonts.scss";
.additional__link {
  color: $white;
  text-transform: uppercase;
  @include primaryText;

  &:hover {
    color: $white;
  }
}
</style>


 <script>
export default {
  name: "AdditionalItem",
  props: {
    additionalStorage: {
      type: Object
    }
  }
};
</script>
