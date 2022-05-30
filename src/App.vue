<template>
  <div id="app">
    <AppHeader />
    <AppMain />
    <AppFooter />
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
          active: false,
        },
        {
          url: "#",
          text: "PAges",
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
      this.headerLinks.forEach((element, index) => {
        this.headerLinks[index].active = false;
      });
      this.headerLinks[index].active = !this.headerLinks[index].active;
    },
  },
};
</script>

<style lang="scss">
@import "./style/commons.scss";
@import "./style/variables.scss";
</style>
