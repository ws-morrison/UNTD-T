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



<style lang="scss">
@import "../assets/scss/variables.scss";
@import "../assets/scss/fonts.scss";
.products {
  &__item {
    width: 340px;
    padding-left: 35px;
    padding-right: 35px;
    padding-top: 40px;
    padding-bottom: 30px;
  }
  &__thumb {
    display: block;
    margin: 0 auto;
    margin-bottom: 25px;
  }
  &__item-title {
    @include primaryTitle;
    text-align: center;
    margin-bottom: 15px;
  }
  &__item-text {
    @include smallText;
    text-align: center;
  }
}
</style>



<script>
export default {
  name: "ProductsCard",
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