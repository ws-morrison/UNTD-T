<template>
  <div class="products__item">
    <img :src="productsStorage.item.thumb" alt class="products__thumb">
    <h4 class="products__item-title">{{productsStorage.item.title}}</h4>
    <p class="products__item-text">
      {{productsStorage.item.lead}}
      <a
        :href="productsStorage.item.link.url"
      >{{productsStorage.item.link.name}}</a>
    </p>
  </div>
</template>


<script>
export default {
  name: "TheProductsCard",
  props: {
    productsStorage: {
      type: Object
    },
    links: {
      type: Object
    }
  }
};
</script>


<style lang="scss">
.products__item {
  width: 340px;
  padding-left: 35px;
  padding-right: 35px;
  padding-top: 40px;
  padding-bottom: 30px;
  // margin-bottom: 20px;
}
.products__thumb {
  display: block;
  margin: 0 auto;
  margin-bottom: 25px;
}
.products__item-title {
  font-family: "PT Sans";
  font-style: normal;
  font-weight: bold;
  font-size: 18px;
  line-height: normal;
  text-align: center;
  margin-bottom: 15px;
}
.products__item-text {
  font-family: "PT Sans";
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: normal;
  text-align: center;
}
</style>
