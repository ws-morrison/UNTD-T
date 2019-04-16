<template>
  <main class="main">
    <solutions></solutions>
    <products></products>
    <worldwide></worldwide>
  </main>
</template>


<script>
import Solutions from "./Solutions";
import Products from "./Products";
import Worldwide from "./Worldwide";

export default {
  name: "TheMain",
  components: {
    Solutions,
    Products,
    Worldwide
  }
};
</script>