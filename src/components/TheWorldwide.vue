<template>
  <section class="worldwide container">
    <h3 class="worldwide__title">Wordlwide recognition</h3>
    <div class="worldwide__content">
      <p
        class="worldwide__text"
      >Integer bibendum turpis sit amet pretium commodo. Cras justo elit, dapibus at viverra non, dapibus vitae est.</p>

      <p
        class="worldwide__text"
      >Fusce pretium enim sit amet elementum eleifend. Quisque at dui nunc. Curabitur sodales, turpis at luctus suscipit, nisl leo dignissim turpis, quis blandit justo nulla sed nisi. Vivamus urna eros, malesuada non massa sed, vestibulum maximus dui. Fusce facilisis nunc a urna lacinia, nec sagittis felis efficitur. Phasellus commodo porttitor odio, eu commodo nisi vehicula ut. Maecenas congue nisi lorem, et maximus ante vestibulum eu. Vivamus non imperdiet ex.</p>
    </div>

    <div class="worldwide__list">
      <the-worldwide-item
        :companyList="item"
        :key="companyList.item"
        v-for="(item, companyList) in companyList"
      ></the-worldwide-item>
    </div>
  </section>
</template>

<script>
import TheWorldwideItem from "./TheWorldwideItem";
export default {
  name: "TheWorldwide",
  components: {
    TheWorldwideItem
  },
  data() {
    return {
      companyList: [
        {
          item: {
            link: "",
            img: "./static/img/worldwide/image_01.png"
          }
        },
        {
          item: {
            link: "",
            img: "./static/img/worldwide/image_02.png"
          }
        },
        {
          item: {
            link: "",
            img: "./static/img/worldwide/image_03.png"
          }
        },
        {
          item: {
            link: "",
            img: "./static/img/worldwide/image_04.png"
          }
        },
        {
          item: {
            link: "",
            img: "./static/img/worldwide/image_05.png"
          }
        }
      ]
    };
  }
};
</script>


<style lang="scss">
.worldwide {
    margin-bottom: 70px;
}
.worldwide__title {
  font-family: "PT Sans";
  font-style: normal;
  font-weight: bold;
  font-size: 18px;
  line-height: normal;
  text-align: center;
  margin-bottom: 30px;
}
.worldwide__content {
  margin-bottom: 35px;
}
.worldwide__text {
  font-family: "PT Sans";
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: normal;
  margin-bottom: 20px;
}
.worldwide__list {
  display: flex;
  width: 70%;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
  margin: 0 auto;
}
</style>
