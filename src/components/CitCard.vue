<template>
  <section class="cit">
    <div class="container">
      <img src="../assets/img/h1-img-01.jpg" alt="people's talking" />
      <div class="cit__card">
        <h4 class="title">Jason Bickford</h4>
        <h6 class="text">Founder and Executive Director</h6>
        <div class="line"></div>
        <p class="text">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae eaque
          saepe. Minima, nulla animi deserunt reiciendis ullam autem
        </p>
        <div class="social">
          <i class="fab fa-linkedin-in"></i>
          <i class="fab fa-facebook-f"></i>
          <i class="fab fa-twitter"></i>
          <div class="sign">Jason Brick</div>
        </div>
      </div>
      <img class="svg" src="../assets/svg/svg-4.svg" alt="" />
    </div>
  </section>
</template>

<script>
export default {
  name: "CitCard",
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
.cit {
  position: relative;
  img {
    width: 50%;
  }
  .svg {
    width: 20%;
    position: absolute;
    top: -2rem;
    right: 15rem;
  }
  &__card {
    position: absolute;
    top: 5rem;
    left: 45%;
    right: 20%;
    z-index: 10;
    background-color: $bg-color-01;
    display: inline-block;
    padding: 6rem 4rem;
    .title {
      font-size: 2rem;
    }
    h6 {
      font-size: 0.8rem;
    }
    .sign {
      display: inline;
      font-size: 2.5rem;
      color: $txt-color-08;
      margin-left: 18rem;
    }
    .social i {
      background-color: $bg-color-08;
      color: $txt-color-01;
    }
  }
}
</style>
