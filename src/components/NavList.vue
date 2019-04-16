<template>
  <ul class="navbar__list row">
    <nav-item :links="item" :key="links.linkItem" v-for="(item, links) in links"></nav-item>
  </ul>
</template>


<style lang="scss">
@import "../assets/scss/variables.scss";
.navbar__list {
  list-style: none;
  padding: 0;
  margin: 0;
  width: 100%;
  max-width: 768px;
  justify-content: space-around;
  flex-wrap: wrap;
  @media (max-width: $laptop) {
    flex-direction: column;
    text-align: center;
    max-width: unset;
    padding-left: 20px;
    padding-right: 20px;
  }
}
</style>



<script>
import NavItem from "./NavItem";
export default {
  name: "NavList",
  components: {
    NavItem
  },
  data() {
    return {
      // $storage
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
