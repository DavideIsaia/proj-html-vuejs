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
          <div class="meeting clearfix">
            <div class="date">
              <div class="day">07</div>
              <div class="month">Jan. 2022</div>
            </div>
            <div class="col-right">
              <h6>Melbourne Coaching</h6>
              <div>
                <i class="far fa-clock"></i
                ><span class="text">9:00 am - 5:00 pm, Jan 7, 2022</span>
              </div>
              <div>
                <i class="fas fa-map-marker-alt"></i
                ><span class="text">Cambridge, MA 02138, USA</span>
              </div>
              <div class="read-more">read more</div>
            </div>
          </div>
        </div>
      </div>
    </section>
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
    padding: 6rem 0;
    .calendar {
      width: 40%;
      background-color: $bg-color-04;
      .title {
        padding: 1.5rem 3rem;
        font-size: 1.8rem;
        border-bottom: 2px solid $bdr-color-03;
      }
      .meeting {
        background-color: $bg-color-04;
        padding: 3rem 0;
        border-bottom: 2px solid $bdr-color-03;
        .date {
          float: left;
          padding: 1rem;
          background-color: $bg-color-08;
          color: white;
          text-align: center;
          margin-left: 3rem;
          .day {
            font-size: 1.6rem;
          }
          .month {
            font-family: "Lato", sans-serif;
            font-size: 0.8rem;
          }
        }
        .col-right {
          float: left;
          padding-left: 1rem;
          text-align: left;
          line-height: 2rem;
          h6 {
            font-size: 1.4rem;
          }
          i {
            margin-right: 1rem;
            color: $txt-color-08;
          }
          span {
            font-size: 1rem;
          }
        }
      }
    }
  }
}
</style>
