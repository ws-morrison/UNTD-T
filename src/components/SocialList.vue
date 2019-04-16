<template>
  <div class="social-list">
    <a href class="social-list__link">
      Facebook
      <icon-facebook></icon-facebook>
    </a>
    <a href class="social-list__link">
      Twitter
      <icon-twitter></icon-twitter>
    </a>
    <a href class="social-list__link">
      Instagram
      <icon-instagram></icon-instagram>
    </a>
  </div>
</template>


<style lang="scss">
@import "../assets/scss/variables.scss";

.social-list {
  display: flex;
  width: 210px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin: 0 auto;
  margin-bottom: 30px;
  &__link {
    width: 50px;
    height: 50px;
    background-color: rgba(255, 255, 255, 0.3);
    border-radius: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 0;
    &:hover {
      border: 2px solid $accientColor;
      background-color: $primaryColor;
    }
  }
}
</style>


<script>
import IconFacebook from "./icons/IconFacebook";
import IconTwitter from "./icons/IconTwitter";
import IconInstagram from "./icons/IconInstagram";
export default {
  name: "TheSocialList",
  components: {
    IconFacebook,
    IconTwitter,
    IconInstagram
  }
};
</script>
