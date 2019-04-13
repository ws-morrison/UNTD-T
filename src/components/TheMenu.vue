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
    <div class="nav__wrapper" :class="{'show': !isActive, 'hidden': isActive}">
      <the-nav></the-nav>
    </div>
  </div>
</template>

<script>
import TheNav from "./TheNav";

export default {
  name: "TheMenu",
  components: {
    TheNav
  },
  data() {
    return {
      isActive: true
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
.menu__wrapper {
  display: flex;
  flex-direction: row;
  width: 100%;
  align-items: center;
  justify-content: space-between;
  @media (max-width: 1024px) {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }
}

.mobile-menu__wrapper {
  margin-right: 120px;
  @media (max-width: 1024px) {
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
  @media (max-width: 1024px) {
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 30px;
  }
}
.drop-menu__list {
  list-style: none;
  padding: 0;
  margin: 0;
  width: 100%;
  max-width: 768px;
  justify-content: space-around;
  flex-wrap: wrap;
  @media (max-width: 1024px) {
    flex-direction: column;
    margin-bottom: 30px;
    text-align: right;
    max-width: unset;
    padding-left: 20px;
    padding-right: 20px;
  }
}
.drop-menu__list-item:nth-child(4) {
  margin-right: 100px;
  @media (max-width: 1024px) {
    margin-right: 0;
    margin-bottom: 30px;
  }
}
.drop-menu__list-link {
  @include primaryText;
  text-decoration: none;
  position: relative;
  color: #fff;
  &:hover {
    color: #fff;
  }
}

.drop-menu__sub-link {
  @include primaryText;
  text-decoration: none;
  position: relative;
  color: rgb(129, 129, 129);
  display: block;
  margin-bottom: 5px;
  &:hover {
    color: #232e4a;
    text-decoration: none;
  }
}
.drop-menu__sub-list {
  position: absolute;
  width: 220px;
  list-style: none;
  background-color: #ffffff;
  padding: 10px;
  border-radius: 4px;
  border: 1px solid rgb(145, 145, 145);
}

// Burger and animation
.burger {
  width: 25px;
  position: relative;
  z-index: 2;
  @media (min-width: 1024px) {
    display: none;
  }
}

.burger-item {
  height: 0.1em;
  background: #ffffff;
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
  background: #fff;
  margin-bottom: 4px;
  transform: rotate(90deg);
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
