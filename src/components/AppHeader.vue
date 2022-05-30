<template>
  <header>
    <nav class="flex">
      <div class="logo">
        <img src="../assets/img/logo-img-01.png" alt="Everlead logo" />
      </div>
      <ul>
        <li
          class="text bold"
          @click="$emit('isActive')"
          v-for="(element, index) in headerLinks"
          :key="index"
          :class="{ active: element.active }"
        >
          <a href="">{{ element.text }}</a>
        </li>
        <li>
          <a href=""><i class="fas fa-search"></i></a>
        </li>
        <li>
          <a href=""><i class="fas fa-list"></i></a>
        </li>
      </ul>
    </nav>
    <div class="cta flex">
      <div class="container">
        <div class="title bold">Our Team<span>.</span></div>
        <p class="text">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Ad excepturi
          soluta nesciunt vitae nobis, inventore beatae laboriosam deserunt.
        </p>
        <button class="white">Read More</button>
        <button class="orange">Purchase</button>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
  // prelevo l'array dal genitore
  props: {
    headerLinks: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
nav {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  width: 90%;
  height: 120px;
  margin: 0 auto;
  img {
    width: 60%;
    padding: 2rem;
  }
  li {
    display: inline-block;
    margin: 0 1.5rem;
    text-transform: uppercase;
    line-height: 120px;
    cursor: pointer;
    color: $txt-color-14;
    font-size: 0.9rem;

    &.active,
    &:hover {
      a {
        color: $txt-color-08;
      }
    }
    &.active {
      &::before {
        content: url("../assets/svg/svg-6.svg");
        filter: invert(55%) sepia(100%) saturate(3.5);
      }
    }
  }
}

.cta {
  background-image: url("../assets/img/rev-slider-main-home-img-03.jpg");
  background-size: cover;
  background-position: center;
  height: 1000px;
  .title {
    font-size: 6rem;
    color: $txt-color-12;
    span {
      color: $txt-color-08;
    }
  }
  .text {
    width: 45%;
    font-size: 1.3rem;
    font-weight: 300;
    color: $txt-color-09;
    line-height: 2rem;
  }

  .white {
    background-color: $bg-color-01;
  }

  .orange {
    background-color: $bg-color-08;
    color: $txt-color-01;
  }
}
</style>
