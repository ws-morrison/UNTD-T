<template>
  <li class="navbar__list-item">
    <a v-bind:href="links.linkItem.itemUrl" class="navbar__list-link">{{links.linkItem.name}}</a>
    <icon-vector v-if="links.linkItem.thumb"></icon-vector>
  </li>
</template>


<style lang="scss">
@import "../assets/scss/variables.scss";
@import "../assets/scss/fonts.scss";
.navbar {
  &__list-item {
    color: $white;
    &:nth-child(4) {
      margin-right: 110px;
      @media (max-width: $laptop) {
        margin-right: 0;
        margin-bottom: 30px;
      }
    }
  }
  &__list-link {
    @include primaryText;
    text-decoration: none;
    position: relative;
    color: $white;
    &:hover {
      color: $white;
    }
  }
}
</style>


<script>
import IconVector from "./icons/IconVector";
export default {
  name: "NavItem",
  components: {
    IconVector
  },
  props: {
    links: {
      type: Object
    }
  }
};
</script>