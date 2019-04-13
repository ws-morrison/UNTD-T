<template>
  <li class="drop-menu__list-item">
    <a v-bind:href="links.linkItem.itemUrl" class="drop-menu__list-link">{{links.linkItem.name}}</a>
    <icon-vector v-if="links.linkItem.thumb"></icon-vector>
  </li>
</template>

<script>
import IconVector from "./icons/IconVector";
export default {
  name: "TheNavItem",
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



