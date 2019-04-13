<template>
  <li class="additional__item">
    <a :href="additionalStorage.item.url" class="additional__link">{{additionalStorage.item.name}}</a>
  </li>
</template>


<script>
export default {
  name: "TheAdditionalItem",
  props: {
    additionalStorage: {
      type: Object
    }
  }
};
</script>


<style lang="scss">
.additional__link {
  color: #fff;
  text-transform: uppercase;

  font-family: "PT Sans";
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: normal;
  &:hover {
    color: #fff;
  }
}
</style>
