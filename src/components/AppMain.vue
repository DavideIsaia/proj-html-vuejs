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
    <!-- section upcoming events -->
    <section class="events">
      <div class="container">
        <div class="calendar">
          <div class="title bold">Upcoming Events</div>
          <CalendarCard
            v-for="(element, index) in meetings"
            :key="index"
            :element="element"
          />
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import SpecCard from "./SpecCard.vue";
import CitCard from "./CitCard.vue";
import CalendarCard from "./CalendarCard.vue";
export default {
  name: "AppMain",
  components: {
    SpecCard,
    CitCard,
    CalendarCard,
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
      meetings: [
        {
          day: "07",
          month: "Jan. 2022",
          title: "Melbourne Coaching",
          hour: "9:00 am - 5:00 pm, Jan 7, 2022",
          place: "Cambridge, MA 02138, USA",
        },
        {
          day: "11",
          month: "Jan. 2022",
          title: "New York Coaching",
          hour: "9:00 am - 5:00 pm, Jan 11, 2022",
          place: "Cambridge, MA 02138, USA",
        },
        {
          day: "21",
          month: "Jan. 2022",
          title: "London Coaching",
          hour: "9:00 am - 5:00 pm, Jan 21, 2022",
          place: "Cambridge, MA 02138, USA",
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
  .events {
    background-image: url("../assets/img/h1-img-09.jpg");
    background-size: cover;
    background-position: center;
    margin-top: 5rem;
    padding: 12rem 0;
    .calendar {
      width: 40%;
      background-color: $bg-color-04;
      .title {
        padding: 1.5rem 3rem;
        font-size: 1.8rem;
        border-bottom: 2px solid $bdr-color-03;
      }
    }
  }
}
</style>
