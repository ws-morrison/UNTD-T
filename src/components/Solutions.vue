<template>
  <section class="solutions container">
    <h3 class="solutions__title">{{title}}</h3>
    <div class="solutions__wrapper row">
      <solution-item
        :solutionsStorage="cards"
        :key="solutionsStorage.item"
        v-for="(cards, solutionsStorage) in solutionsStorage"
      ></solution-item>
    </div>
  </section>
</template>


<style lang="scss">
@import "../assets/scss/variables.scss";
@import "../assets/scss/fonts.scss";

.solutions {
  margin-bottom: 80px;
  &__title {
    @include primaryTitle;
    text-align: center;
    margin: 0;
    padding: 0;
    display: block;
    margin-bottom: 32px;
  }
  &__wrapper {
    width: 100%;
    justify-content: space-around;
  }
}
</style>


<script>
import SolutionItem from "./SolutionItem";
export default {
  name: "TheSolutions",
  components: {
    SolutionItem
  },
  data() {
    return {
      title: "Etiam ac nisl ac quam sodales scelerisque elementum quis purus.",
      solutionsStorage: [
        {
          item: {
            thumb: "./static/img/solutions/solutions_0.png",
            title: "Donec efficitur molestie",
            lead:
              "Nulla pretium nunc in nulla placerat, sit amet porttitor enim ullamcorper. Curabitur ex erat, euismod ac vestibulum vel, viverra non lorem.",
            linkName: "Learn More",
            link: "https://google.com"
          }
        },
        {
          item: {
            thumb: "./static/img/solutions/solutions_1.png",
            title: "Mauris interdum venenatis",
            lead:
              "Vivamus cursus ante eu orci rutrum, vitae viverra ante dapibus. Vivamus porta molestie turpis, quis elementum nisi egestas eget.",
            linkName: "Learn More",
            link: "https://google.com"
          }
        },
        {
          item: {
            thumb: "./static/img/solutions/solutions_2.png",
            title: "Cras sit amet",
            lead:
              "Fusce suscipit, ante at imperdiet vehicula, ex augue feugiat enim, sed faucibus sem tortor quis turpis. Mauris lacinia neque id augue efficitur, ut feugiat massa efficitur.",
            linkName: "Learn More",
            link: "https://google.com"
          }
        }
      ]
    };
  }
};
</script>

