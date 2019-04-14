<template>
  <header class="header" :style="{ backgroundImage: 'url(' + backgroundImg + ')' }">
    <div class="container">
      <nav class="header-nav">
        <the-menu></the-menu>
      </nav>
      <div class="heading">
        <h1 class="heading__title">
          We solve
          <br>your problems
        </h1>
        <p class="heading__text">{{headingText}}</p>
      </div>
    </div>
  </header>
</template>


<style lang="scss">
.header {
  background-color: #1d2741;
  background-size: 1440px 100%;
  padding-top: 25px;
  padding-bottom: 100px;
  margin-bottom: 80px;
  @media (min-width: 1440px) {
    background-repeat: repeat-x;
    background-size: 100%;
  }
}
.header-nav {
  display: flex;
  width: 100%;
  justify-content: space-around;
  margin-bottom: 85px;
  align-items: center;
}

.heading__title {
  font-family: "Open Sans", Helvetica, sans-serif;
  font-size: 48px;
  text-align: center;
  margin: 0 auto;
  color: #fff;
  margin-bottom: 85px;
  text-transform: uppercase;
}

.heading__text {
  font-family: "PT Sans", Helvetica, sans-serif;
  font-weight: 400;
  font-size: 18px;
  text-align: center;
  padding: 0;
  margin: 0;
  color: #fff;
}
</style>


<script>
import TheMenu from "./TheMenu";
export default {
  name: "TheHeader",
  components: {
    TheMenu
  },
  data: function() {
    return {
      backgroundImg: "/static/img/main-bg.jpg",
      headingTitle: "We solve your problems",
      headingText:
        "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Molestias magnam maiores possimus quo totam odio quibusdam voluptate ea doloribus nemo odit facilis reprehenderit, architecto laborum, laudantium omnis repellendus tempora nam?"
    };
  }
};
</script>

