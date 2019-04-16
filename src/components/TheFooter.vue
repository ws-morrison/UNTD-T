<template>
  <footer class="footer">
    <div class="container">
      <ul class="additional-list">
        <additional-item
          :additionalStorage="item"
          :key="additionalStorage.item"
          v-for="(item, additionalStorage) in additionalStorage"
        ></additional-item>
      </ul>
      <social-list></social-list>
    </div>
    <span class="footer__copyright">Copright © 1999 - 2019</span>
  </footer>
</template>


<style lang="scss">
@import "../assets/scss/variables.scss";
@import "../assets/scss/fonts.scss";
.footer {
  background-color: $primaryColor;
  padding-top: 40px;
  padding-bottom: 54px;
}

.footer__copyright {
  @include primaryTextBold;
  color: $white;
  text-align: center;
  display: block;
  margin: 0 auto;
}
.additional-list {
  display: flex;
  width: 35%;
  min-width: 300px;
  justify-content: space-around;
  justify-items: center;
  margin: 0;
  padding: 0;
  margin: 0 auto;
  list-style: none;
  margin-bottom: 25px;
}
</style>



<script>
import AdditionalItem from "./AdditionalItem";
import SocialList from "./SocialList";
export default {
  name: "TheFooter",
  components: {
    AdditionalItem,
    SocialList
  },
  data() {
    return {
      additionalStorage: [
        {
          item: {
            name: "Privacy Policy",
            url: "https://google.com"
          }
        },
        {
          item: {
            name: "About Us",
            url: "https://google.com"
          }
        },
        {
          item: {
            name: "Support",
            url: "https://google.com"
          }
        }
      ]
    };
  }
};
</script>