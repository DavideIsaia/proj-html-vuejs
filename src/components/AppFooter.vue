<template>
  <footer>
    <div class="container clearfix">
      <div class="left">
        <h4 class="title">About</h4>
        <div class="line"></div>
        <p class="text">
          We created Everlead to effectively become the stepping stone torwards
          meeting all your goals &#38; achievinf business success.
        </p>
        <div class="social">
          <i class="fab fa-linkedin-in"></i>
          <i class="fab fa-facebook-f"></i>
          <i class="fab fa-twitter"></i>
        </div>
      </div>
    </div>
    <div class="copyright text">CopyrightEverlead&copy;MikadoThemes</div>
  </footer>
</template>

<script>
export default {
  name: "AppFooter",
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
footer {
  background-color: $bg-color-15;
  .container {
    padding: 8rem 0;
  }
  .left {
    width: 20%;
    padding-right: 2rem;
    .title {
      color: $txt-color-01;
      font-size: 1.2rem;
    }
    .line {
      width: 2rem;
      margin: 1rem 0;
    }
    .text {
      font-size: 0.9rem;
      color: $txt-color-07;
      line-height: 1.5rem;
    }
    .social i {
      background-color: $bg-color-01;
      color: $txt-color-13;
      margin-top: 2rem;
      &:hover {
        color: $txt-color-01;
        background-color: $bg-color-08;
      }
    }
  }
}
.copyright {
  background-color: $bg-color-08;
  color: $txt-color-01;
  padding: 0.4rem;
  text-align: center;
  font-size: 0.9rem;
}
</style>
