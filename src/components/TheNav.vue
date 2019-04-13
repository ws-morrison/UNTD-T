<template>
  <ul class="drop-menu__list row">
    <the-nav-item :links="item" :key="links.linkItem" v-for="(item, links) in links"></the-nav-item>
  </ul>
</template>


<script>
import TheNavItem from "./TheNavItem";

export default {
  name: "TheNav",
  components: {
    TheNavItem
  },
  data() {
    return {
      links: [
        {
          linkItem: {
            name: "Products",
            itemUrl: "",
            thumb: true
          }
        },
        {
          linkItem: {
            name: "News & Events",
            itemUrl: "https://github.com"
          }
        },
        {
          linkItem: {
            name: "Support",
            itemUrl: "https://yandex.com"
          }
        },
        {
          linkItem: {
            name: "Contacts",
            itemUrl: "https://habr.com"
          }
        },
        {
          linkItem: {
            name: "Login",
            itemUrl: "https://habr.com"
          }
        },
        {
          linkItem: {
            name: "Buy Now",
            itemUrl: "https://habr.com"
          }
        }
      ]
    };
  }
};
</script>


<style lang="scss">
@mixin primaryText {
  font-family: "PT Sans", "Helvetica", sans-serif;
  font-weight: 400;
  font-size: 16px;
}
@media (max-width: 1024px) {
  .show {
    display: block;
  }

  .hidden {
    display: none;
  }
}
</style>
