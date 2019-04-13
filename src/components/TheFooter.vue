<template>
  <footer class="footer">
    <div class="container">
      <ul class="additional-list">
        <the-additional-item
          :additionalStorage="item"
          :key="additionalStorage.item"
          v-for="(item, additionalStorage) in additionalStorage"
        ></the-additional-item>
      </ul>
      <the-social-list></the-social-list>
    </div>
    <span class="footer__copyright">Copright © 1999 - 2019</span>
  </footer>
</template>


<script>
import TheAdditionalItem from "./TheAdditionalItem";
import TheSocialList from "./TheSocialList";
export default {
  name: "TheFooter",
  components: {
    TheAdditionalItem,
    TheSocialList
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


<style lang="scss">
.footer {
  background-color: #1d2741;
  padding-top: 40px;
  padding-bottom: 54px;
}

.footer__copyright {
  font-family: "PT Sans";
  font-style: normal;
  font-weight: bold;
  font-size: 15px;
  line-height: normal;
  color: #ffffff;
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
