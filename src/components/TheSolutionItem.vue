<template>
  <div class="solutions__item">
    <img :src="solutionsStorage.item.thumb" alt class="solutions__thumb">
    <h4 class="solutions__item-title">{{solutionsStorage.item.title}}</h4>
    <p class="solutions__item-text">{{solutionsStorage.item.lead}}</p>
    <a href class="solutions__item-link">{{solutionsStorage.item.linkName}}</a>
  </div>
</template>


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


<style lang="scss">
.solutions__item {
  width: 340px;
  background-color: #fafafa;
  padding-left: 35px;
  padding-right: 35px;
  padding-top: 40px;
  padding-bottom: 30px;
  margin-bottom: 20px;
}
.solutions__thumb {
  display: block;
  margin: 0 auto;
  margin-bottom: 25px;
}
.solutions__item-title {
  font-family: "PT Sans";
  font-style: normal;
  font-weight: bold;
  font-size: 18px;
  line-height: normal;
  text-align: center;
  margin-bottom: 15px;
}
.solutions__item-text {
  font-family: "PT Sans";
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: normal;
  margin-bottom: 30px;
}
.solutions__item-link {
  display: block;
  text-align: center;
}
</style>
