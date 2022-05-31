<template>
  <section class="testimonials">
    <h3 class="title bold">Testimonials<span>.</span></h3>
    <div class="overlay">
      <img src="../assets/img/h3-img-04.png" alt="Cynthia Clark" />
      <div class="title bold">Cynthia Clark</div>
      <p class="text">
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Illum officia
        error quos id sunt quis quae dolor nulla alias.
      </p>
      <div class="active-img">
        <span class="text">01</span>
        <div class="progress-bar">
          <div class="elapsed"></div>
        </div>
        <span class="text">03</span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "TestimonialsCard",
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
.testimonials {
  text-align: center;
  position: relative;
  h3 {
    font-size: 15rem;
  }
  .overlay {
    position: absolute;
    top: 4rem;
    left: 0;
    width: 100%;
    background-color: #1e1c1cf0;
    padding: 8rem;
    .title,
    .text,
    span {
      color: $txt-color-01;
    }
    p {
      margin: 0.5rem auto;
      width: 40%;
    }
    img {
      width: 8%;
      border-radius: 50%;
      margin-bottom: 1rem;
    }
    .active-img {
      display: flex;
      justify-content: space-between;
      align-items: center;
      width: 15%;
      margin: 2rem auto;
      span {
        font-size: 0.8rem;
        margin: 0 2em;
      }
    }
    .progress-bar {
      position: relative;
      height: 1px;
      width: 100%;
      background-color: $txt-color-11;
    }
    .elapsed {
      position: absolute;
      left: 0;
      width: 33%;
      height: 100%;
      background-color: $bg-color-07;
    }
  }
}
</style>
