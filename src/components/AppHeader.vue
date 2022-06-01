<template>
  <header>
    <!-- navbar -->
    <nav class="flex">
      <div class="logo">
        <img src="../assets/img/logo-img-01.png" alt="Everlead logo" />
        <!-- hover logo -->
        <img
          class="hide"
          src="../assets/img/logo-img-02.png"
          alt="Everlead logo bloack"
        />
      </div>
      <!-- links dinamici menu -->
      <ul>
        <li
          class="text"
          @click="$emit('isActive', index)"
          v-for="(element, index) in headerLinks"
          :key="index"
          :class="{ active: element.active }"
        >
          <!-- svg freccia classe active menu -->
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
        <!-- icone menu -->
        <li>
          <a href=""><i class="fas fa-search"></i></a>
        </li>
        <li>
          <a href=""><i class="fas fa-list"></i></a>
        </li>
      </ul>
    </nav>
    <!-- call to action -->
    <div class="cta flex">
      <div class="container">
        <h2 class="title bold">Our Team<span>.</span></h2>
        <p class="text">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Ad excepturi
          soluta nesciunt vitae nobis, inventore beatae laboriosam deserunt.
        </p>
        <button class="white">
          <span>Read More</span
          ><svg
            xmlns="http://www.w3.org/2000/svg"
            width="60"
            height="32"
            style="height: 22px"
            fill="black"
          >
            <path
              d="M4 15a1 1 0 001 1h19.586l-4.292 4.292a1 1 0 001.414 1.414l6-6a.99.99 0 00.292-.702V15c0-.13-.026-.26-.078-.382a.99.99 0 00-.216-.324l-6-6a1 1 0 00-1.414 1.414L24.586 14H5a1 1 0 00-1 1z"
            />
          </svg>
        </button>
        <button class="orange">
          <span>Purchase</span
          ><svg
            xmlns="http://www.w3.org/2000/svg"
            width="60"
            height="32"
            style="height: 22px"
            fill="white"
          >
            <path
              d="M4 15a1 1 0 001 1h19.586l-4.292 4.292a1 1 0 001.414 1.414l6-6a.99.99 0 00.292-.702V15c0-.13-.026-.26-.078-.382a.99.99 0 00-.216-.324l-6-6a1 1 0 00-1.414 1.414L24.586 14H5a1 1 0 00-1 1z"
            />
          </svg>
        </button>
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
// navbar
nav {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  width: 90%;
  height: 120px;
  margin: 0 auto;
  .logo {
    position: relative;
    width: 200px;
    &:hover {
      .hide {
        display: block;
        cursor: pointer;
        background-color: $bg-color-12;
      }
    }
  }
  img {
    position: absolute;
    top: -2rem;
    left: 0;
    width: 100%;
    padding: 0.8rem 1rem;
  }
  .hide {
    display: none;
  }
  // links menu
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
// call to action
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
  // buttons
  .white {
    background-color: $bg-color-01;
    span {
      padding: 0.8rem;
      border-right: 2px solid black;
    }
    svg {
      padding: 0 1rem;
    }
    &:hover {
      span {
        border-right: 2px solid transparent;
      }
    }
  }
  .orange {
    background-color: $bg-color-08;
    color: $txt-color-01;
    span {
      padding: 0.8rem;
      border-right: 2px solid white;
    }
    svg {
      padding: 0 1rem;
    }
    &:hover {
      span {
        border-right: 2px solid transparent;
      }
    }
  }
}
</style>
