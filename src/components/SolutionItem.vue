<template>
  <div class="solutions__item">
    <img :src="solutionsStorage.item.thumb" alt class="solutions__thumb">
    <h4 class="solutions__item-title">{{solutionsStorage.item.title}}</h4>
    <p class="solutions__item-text">{{solutionsStorage.item.lead}}</p>
    <a href class="solutions__item-link">{{solutionsStorage.item.linkName}}</a>
  </div>
</template>


<style lang="scss">
@import "../assets/scss/variables.scss";
@import "../assets/scss/fonts.scss";
.solutions {
  &__item {
    width: 340px;
    background-color: #fafafa;
    padding-left: 35px;
    padding-right: 35px;
    padding-top: 40px;
    padding-bottom: 30px;
    margin-bottom: 20px;
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
    margin-bottom: 30px;
  }
  &__item-link {
    display: block;
    text-align: center;
  }
}
</style>


<script>
export default {
  name: "TheSolutionItem",
  props: {
    solutionsStorage: {
      type: Object
    }
  }
};
</script>