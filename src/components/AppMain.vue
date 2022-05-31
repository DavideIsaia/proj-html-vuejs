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
    <!-- section creative leader -->
    <section class="creative">
      <div class="container clearfix">
        <div class="col-left">
          <h4 class="title bold">Creative Leader<span>.</span></h4>
          <div class="line"></div>
          <p class="text">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam
            minima illo veritatis ea, odio eius. Fugiat inventore placeat amet
            assumenda autem fuga est modi, voluptatum dolorem exercitationem,
            quam sit voluptatem? Lorem ipsum dolor sit amet consectetur
            adipisicing elit. Illo laborum, recusandae nisi provident fugiat
            numquam culpa dolor minima velit nesciunt doloremque ullam
          </p>
          <div class="read-more">read more</div>
        </div>
        <div class="col-right">
          <div class="bar-container clearfix">
            <h5 class="title bold left">Mentorship</h5>
            <h5 class="title bold right">78%</h5>
            <div class="progress-bar">
              <div class="filled"></div>
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
      bars: [
        {
          title: "Mentorship",
          percentage: 78,
        },
        {
          title: "Education",
          percentage: 95,
        },
        {
          title: "Learning",
          percentage: 65,
        },
        {
          title: "Motivation",
          percentage: 83,
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
  .creative {
    padding: 5rem 0;
    background-color: $bg-color-01;
    .col-left {
      float: left;
      width: 45%;
      .title {
        font-size: 3rem;
      }
      .text {
        font-size: 1.1rem;
        padding-bottom: 2rem;
      }
    }
    .col-right {
      float: right;
      width: 45%;
      .bar-container {
        h5 {
          font-size: 1.5rem;
        }
        .left {
          float: left;
        }
        .right {
          float: right;
        }
        .progress-bar {
          position: relative;
          top: 1rem;
          float: left;
          height: 2px;
          width: 100%;
          background-color: $bg-color-07;
        }
        .filled {
          position: absolute;
          left: 0;
          bottom: 0;
          width: 78%;
          height: 3px;
          background-color: $bg-color-08;
        }
      }
    }
  }
}
</style>
