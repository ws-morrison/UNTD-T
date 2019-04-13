<template>
  <section class="products container">
    <h3 class="products__title">{{title}}</h3>
    <p class="products__lead">{{lead}}</p>
    <div class="products__wrapper row">
      <the-products-card
        :productsStorage="cards"
        :key="productsStorage.item"
        v-for="(cards, productsStorage) in productsStorage"
      ></the-products-card>
    </div>
    <the-more-button></the-more-button>
  </section>
</template>


<script>
import TheProductsCard from "./TheProductsCard";
import TheMoreButton from "./TheMoreButton";

export default {
  name: "TheProducts",
  components: {
    TheProductsCard,
    TheMoreButton
  },
  data() {
    return {
      title: "Esodales scelerisque elementum quis purus.",
      lead:
        "Integer bibendum turpis sit amet pretium commodo. Cras justo elit, dapibus at viverra non, dapibus vitae est. Morbi facilisis mi non iaculis porttitor. Phasellus a nibh a lacus dignissim pharetra. Vivamus ullamcorper finibus mauris, sit amet volutpat enim sollicitudin sed.",
      productsStorage: [
        {
          item: {
            thumb: "./static/img/products/icon_04.png",
            title: "Proin felis eros ",
            lead: "Iverra sed eros id, eleifend maximus tortor",
            link: {
              name: "",
              url: ""
            }
          }
        },
        {
          item: {
            thumb: "./static/img/products/icon_05.png",
            title: "Suspendisse potenti",
            lead: "Vestibulum mi risus, aliquam vitae efficitur quis",
            link: {
              name: "",
              url: ""
            }
          }
        },
        {
          item: {
            thumb: "./static/img/products/icon_06.png",
            title: "Fusce pretium enim",
            lead:
              "Quisque at dui nunc. Curabitur sodales, turpis at luctus suscipit, nisl leo dignissim turpis",
            link: ""
          }
        },
        {
          item: {
            thumb: "./static/img/products/icon_07.png",
            title: "Vivamus urna eros",
            lead:
              "Fusce facilisis nunc a urna lacinia, nec sagittis felis efficitur. Phasellus commodo porttitor odio",
            link: {
              name: "",
              url: ""
            }
          }
        },
        {
          item: {
            thumb: "./static/img/products/icon_08.png",
            title: "Cras sit amet",
            lead:
              "Interdum et malesuada fames ac ante ipsum primis in faucibus. Curabitur vulputate arcu nisi",
            link: {
              name: "arcu nisi",
              url: "https://google.com"
            }
          }
        },
        {
          item: {
            thumb: "./static/img/products/icon_09.png",
            title: "Cras sit amet",
            lead:
              "Praesent ac turpis sit amet ex euismod congue vitae sit amet risus",
            link: {
              name: "",
              url: ""
            }
          }
        }
      ]
    };
  }
};
</script>


<style lang="scss">
.products {
  margin-bottom: 80px;
}
.products__title {
  font-family: "PT Sans", "Helvetica", sans-serif;
  font-weight: 700;
  font-size: 18px;
  text-align: center;
  margin: 0;
  padding: 0;
  display: block;
  margin-bottom: 32px;
}
.products__wrapper {
  width: 100%;
  justify-content: space-around;
  align-items: baseline;
}
</style>
