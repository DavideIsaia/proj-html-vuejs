<template>
  <header>
    <nav class="flex">
      <div class="logo">
        <img src="../assets/img/logo-img-01.png" alt="Everlead logo" />
      </div>
      <ul>
        <li
          class="text"
          @click="$emit('isActive', index)"
          v-for="(element, index) in headerLinks"
          :key="index"
          :class="{ active: element.active }"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="32"
            height="32"
            style="height: 22px"
            fill="none"
          >
            <path
              d="M4 15a1 1 0 001 1h19.586l-4.292 4.292a1 1 0 001.414 1.414l6-6a.99.99 0 00.292-.702V15c0-.13-.026-.26-.078-.382a.99.99 0 00-.216-.324l-6-6a1 1 0 00-1.414 1.414L24.586 14H5a1 1 0 00-1 1z"
            />
          </svg>
          <a class="bold" href="">{{ element.text }}</a>
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
        <h2 class="title bold">Our Team<span>.</span></h2>
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
      svg {
        fill: $txt-color-08;
      }
    }
  }
}

.cta {
  background-image: url("../assets/img/rev-slider-main-home-img-03.jpg");
  background-size: cover;
  background-position: center;
  padding-top: 8rem;
  height: 1000px;
  .title {
    font-size: 6rem;
  }
  .text {
    width: 45%;
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
