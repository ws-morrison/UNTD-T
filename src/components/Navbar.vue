<template>
  <div class="menu__wrapper">
    <div class="mobile-menu__wrapper">
      <div class="logo-wrapper">
        <img src="../assets/logo.png" alt="logo" width="249px" height="49px">
      </div>
      <div class="burger" @click="isActive=!isActive" v-bind:class="{'open': !isActive}">
        <div class="burger-item"></div>
        <div class="burger-item burger-item--middle"></div>
        <div class="burger-item"></div>
      </div>
    </div>
    <div class="nav__wrapper" :class="{'showMenu': !isActive, 'hiddenMenu': isActive}">
      <nav-list></nav-list>
    </div>
  </div>
</template>

<style lang="scss">
@import "../assets/scss/variables.scss";
@import "../assets/scss/fonts.scss";

.menu__wrapper {
  display: flex;
  flex-direction: row;
  width: 100%;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 85px;
  @media (max-width: $laptop) {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    margin-bottom: 55px;
  }
}
.logo-wrapper {
  margin-right: 30px;
  @media (max-width: $laptop) {
    margin: 0;
  }
}
.mobile-menu__wrapper {
  @media (max-width: $laptop) {
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 30px;
  }
}
.nav__wrapper {
  display: flex;
  flex-direction: row;
  width: 100%;
  align-items: center;
}

// Burger and animation
.burger {
  width: 25px;
  position: relative;
  z-index: 2;
  @media (min-width: 1025px) {
    display: none;
  }
}
.burger-item {
  height: 0.1em;
  background: $white;
  margin-bottom: 6px;
  transition: 0.3s ease-out;
  border-radius: 8px;
}
.burger-item:last-child {
  margin-bottom: 0;
}
.open .burger-item:first-child {
  transform: scale(0);
}

.open .burger-item:last-child {
  transform: scale(0);
}

.open .burger-item--middle {
  transform: rotate(45deg);
}

.open .burger-item--middle::before {
  position: absolute;
  content: "";
  width: 25px;
  height: 0.1em;
  background: $white;
  margin-bottom: 4px;
  transform: rotate(90deg);
}

@media (max-width: $laptop) {
  .showMenu {
    display: block;
    background-color: $primaryColor;

    top: 0;
    right: 0;
    position: absolute;
    padding-top: 100px;
    padding-bottom: 200px;
    height: 100%;
    box-shadow: 0px 5px 20px 0px rgba(5, 5, 5, 0.774);
  }
  .hiddenMenu {
    display: none;
  }
}
</style>


<script>
import NavList from "./NavList";

export default {
  name: "Menu",
  components: {
    NavList
  },
  data() {
    return {
      isActive: true
    };
  }
};
</script>