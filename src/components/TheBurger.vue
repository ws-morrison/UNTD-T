<template>
  <div class="burger" @click="isActive=!isActive" v-bind:class="{'open': !isActive}">
    <div class="burger-item"></div>
    <div class="burger-item burger-item--middle"></div>
    <div class="burger-item"></div>
  </div>
</template>


<script>
export default {
  name: "TheBurger",
  data() {
    return {
      isActive: true
    };
  }
};
</script>


<style lang="scss">
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
</style>
