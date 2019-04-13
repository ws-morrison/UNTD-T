<template>
  <main class="main">
    <the-solutions></the-solutions>
    <the-products></the-products>
    <the-worldwide></the-worldwide>
  </main>
</template>


<script>
import TheSolutions from "./TheSolutions";
import TheProducts from "./TheProducts";
import TheProductsCard from "./TheProductsCard";
import TheWorldwide from "./TheWorldwide";

export default {
  name: "TheMain",
  components: {
    TheSolutions,
    TheProducts,
    TheProductsCard,
    TheWorldwide
  }
};
</script>