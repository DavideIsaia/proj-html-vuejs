<template>
  <div id="app">
    <!-- header -->
    <AppHeader @isActive="isActive" :headerLinks="headerLinks" />
    <!-- main -->
    <AppMain />
    <!-- footer -->
    <AppFooter />
    <!-- bottoni fixed laterali -->
    <a href="#" class="return-to-top">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="32"
        style="height: 30px"
        fill="orange"
        transform="rotate(270)"
      >
        <path
          d="M4 15a1 1 0 001 1h19.586l-4.292 4.292a1 1 0 001.414 1.414l6-6a.99.99 0 00.292-.702V15c0-.13-.026-.26-.078-.382a.99.99 0 00-.216-.324l-6-6a1 1 0 00-1.414 1.414L24.586 14H5a1 1 0 00-1 1z"
        />
      </svg>
    </a>
    <a href="" class="spin"
      ><svg
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 87 87"
        style="height: 28px"
        fill="white"
      >
        <path
          d="M55.4 81.5c6.1-11.1 5.2-16.1-4.3-24.3 6.1-3.5 9.5-8.5 9.1-15.7-.5-8.2-7.7-14.7-16.3-14.6-8.5.1-15.6 6.7-15.9 15-.3 8.5 5.9 15.8 14.3 16.6 1.4.1 2.8.2 4.2.5 5.9 1.2 10.2 6.7 9.8 12.6-.4 6.4-5.5 11.4-11.8 11.7-19.6.9-38.6-14.8-41.3-34C-.1 26.9 14.4 6.8 36.4 2.8c22.3-4 43.4 10 48.1 32 4.3 20-8.6 41.2-28.4 46.7h-.7z"
        /></svg
    ></a>
    <a href="" class="buy"
      ><svg
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 24 24"
        style="height: 16px"
        fill="#ee2852"
      >
        <circle cx="9" cy="21" r="2" />
        <circle cx="20" cy="21" r="2" />
        <path
          d="M23.8 5.4c-.2-.3-.5-.4-.8-.4H6.8L6 .8C5.9.3 5.5 0 5 0H1C.4 0 0 .4 0 1s.4 1 1 1h3.2L5 6.2v.1l1.7 8.3C7 16 8.2 17 9.6 17H19.4c1.5 0 2.7-1 3-2.4L24 6.2c0-.3 0-.6-.2-.8z"
        /></svg
    ></a>
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    AppMain,
    AppFooter,
  },
  data() {
    return {
      headerLinks: [
        {
          url: "#",
          text: "Homes",
          active: true,
        },
        {
          url: "#",
          text: "Pages",
          active: false,
        },
        {
          url: "#",
          text: "Blog",
          active: false,
        },
        {
          url: "#",
          text: "Shop",
          active: false,
        },
        {
          url: "#",
          text: "Events",
          active: false,
        },
        {
          url: "#",
          text: "Elements",
          active: false,
        },
      ],
    };
  },
  methods: {
    isActive: function (index) {
      this.headerLinks.forEach((element) => {
        element.active = false;
      });
      this.headerLinks[index].active = !this.headerLinks[index].active;
    },
  },
};
</script>

<style lang="scss">
@import "./style/commons.scss";
@import "./style/variables.scss";
.title {
  color: $txt-color-12;
  span {
    color: $txt-color-08;
  }
}
.text {
  font-size: 1.3rem;
  font-weight: 300;
  color: $txt-color-09;
  line-height: 2rem;
}
.return-to-top,
.spin,
.buy {
  position: fixed;
  text-align: center;
}
.spin,
.buy {
  right: 0;
  width: 2.5rem;
  height: 2.5rem;
}
.return-to-top {
  top: 50vh;
  right: 10px;
  width: 3rem;
  height: 3rem;
  background-color: white;
  padding: 0.5rem;
  border-radius: 50%;
  box-shadow: 1px 1px 8px 0px $bg-color-11;
}
.spin {
  top: 35vh;
  background-color: $bg-color-10;
  padding: 0.4rem;
}
.buy {
  top: 40vh;
  background-color: $bg-color-01;
  padding: 0.7rem;
}
</style>
