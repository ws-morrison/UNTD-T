<template>
  <div id="app">
    <the-header></the-header>
    <the-main></the-main>
    <the-footer></the-footer>
  </div>
</template>

<script>
import TheHeader from "./components/TheHeader";
import TheMain from "./components/TheMain";
import TheFooter from "./components/TheFooter";
export default {
  name: "App",
  components: {
    TheHeader,
    TheMain,
    TheFooter
  }
};
</script>

<style lang="scss">
@mixin primaryText {
  font-family: "PT Sans", "Helvetica", sans-serif;
  font-weight: 700;
  font-size: 16px;
}
</style>
