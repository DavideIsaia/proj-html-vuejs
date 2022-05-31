<template>
  <main>
    <!-- section specialties -->
    <section class="spec">
      <div class="container">
        <h3 class="title bold">Our Specialties<span>.</span></h3>
        <p class="text">
          Lorem, ipsum dolor sit amet consectetur adipisicing elit
        </p>
        <div class="line"></div>
        <div class="flex">
          <SpecCard
            v-for="(element, index) in cards"
            :key="index"
            :element="element"
          />
        </div>
      </div>
    </section>
    <!-- section founder's citation -->
    <CitCard />
  </main>
</template>

<script>
import SpecCard from "./SpecCard.vue";
import CitCard from "./CitCard.vue";
export default {
  name: "AppMain",
  components: {
    SpecCard,
    CitCard,
  },
  data() {
    return {
      cards: [
        {
          thumb: "svg-0.svg",
          title: "Knowing",
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit.",
        },
        {
          thumb: "svg-1.svg",
          title: "Selling",
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit.",
        },
        {
          thumb: "svg-2.svg",
          title: "Learning",
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit.",
        },
        {
          thumb: "svg-3.svg",
          title: "Contact",
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit.",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
main {
  background-color: $bg-color-04;
  .spec {
    width: 90%;
    background-color: $bg-color-01;
    position: relative;
    top: -5rem;
    margin: 0 auto;
    text-align: center;
    padding-top: 6rem;
    .line {
      margin-left: auto;
      margin-right: auto;
    }
    .title {
      font-size: 3rem;
    }
  }
}
</style>
