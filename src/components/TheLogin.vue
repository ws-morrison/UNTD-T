<template>
  <div class="login">
    <a href="#" class="login__link">Login</a>
    <a href="#" class="login__link">Buy Now</a>
  </div>
</template>


<script>
export default {
  name: "TheLogin"
};
</script>

<style lang="scss">
@mixin primaryText {
  font-family: "PT Sans", "Helvetica", sans-serif;
  font-weight: 400;
  font-size: 16px;
}

.login {
  display: flex;
  max-width: 130px;
  width: 100%;
  justify-content: space-between;
  @media (max-width: 1024px) {
    max-width: unset;
    flex-direction: column;
    text-align: right;
  }
}

.login__link {
  @include primaryText;
  text-decoration: none;
  color: #fff;
  &:hover {
    color: #fff;
  }
}
</style>
