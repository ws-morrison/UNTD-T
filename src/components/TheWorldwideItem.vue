<template>
  <a href class="worldwide__item">
    <img :src="companyList.item.img" alt class="worldwide__img">
  </a>
</template>


<script>
export default {
  name: "TheWorldwideItem",
  props: {
    companyList: {
      type: Object
    }
  }
};
</script>


<style lang="scss">
.worldwide__item {
  display: block;
  margin-bottom: 50px;
}
</style>
