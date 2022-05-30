<template>
  <header>
    <nav class="flex">
      <div class="logo">
        <img src="../assets/img/logo-img-01.png" alt="Everlead logo" />
      </div>
      <ul>
        <li
          class="text bold"
          @click="isActive(index)"
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
    <div class="cta"></div>
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
    margin: 0 1rem;
    text-transform: uppercase;
    line-height: 120px;
    cursor: pointer;
    color: $txt-color-14;

    &.active,
    &:hover {
      a {
        color: $txt-color-08;
      }
    }
  }
}

.cta {
  background-image: url("../assets/img/rev-slider-main-home-img-03.jpg");
  background-size: cover;
  background-position: center;
  height: 1000px;
}
</style>
