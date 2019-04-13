<template>
  <div class="social-list">
    <a href class="social-list__link">
      <icon-facebook></icon-facebook>
    </a>
    <a href class="social-list__link">
      <icon-twitter></icon-twitter>
    </a>
    <a href class="social-list__link">
      <icon-instagram></icon-instagram>
    </a>
  </div>
</template>


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

<style lang="scss">
.social-list {
  display: flex;
  width: 210px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin: 0 auto;
  margin-bottom: 30px;
}
.social-list__link {
  width: 50px;
  height: 50px;
  background-color: rgba(255, 255, 255, 0.3);
  border-radius: 25px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
