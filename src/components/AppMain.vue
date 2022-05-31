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
            adipisicing.
          </p>
          <div class="read-more">read more</div>
        </div>
        <div class="col-right">
          <ProgressCard
            v-for="(element, index) in bars"
            :key="index"
            :element="element"
          />
        </div>
      </div>
    </section>
    <!-- section latest news -->
    <section class="news">
      <div class="container">
        <h3 class="title bold">Latest News<span>.</span></h3>
        <p class="text">
          Lorem, ipsum dolor sit amet consectetur adipisicing elit
        </p>
        <div class="line"></div>
        <div class="flex">
          <div class="card">
            <div class="card__top">
              <img src="../assets/img/h1-blog-img-02.jpg" alt="" />
              <div class="tag">
                <i class="fas fa-tag"></i><span>Business, Leading</span>
              </div>
            </div>
            <div>
              <i class="far fa-clock"></i>
              <span class="text space">May 5, 2019</span>
              <i class="far fa-user"></i>
              <span class="text">Amanda Doe</span>
            </div>
            <h5 class="title bold">Next Investment</h5>
            <p class="text">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Alias
              tenetur...
            </p>
            <div class="read-more">read more</div>
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
import ProgressCard from "./ProgressCard.vue";
export default {
  name: "AppMain",
  components: {
    SpecCard,
    CitCard,
    CalendarCard,
    ProgressCard,
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
          percentage: "78%",
        },
        {
          title: "Education",
          percentage: "95%",
        },
        {
          title: "Learning",
          percentage: "65%",
        },
        {
          title: "Motivation",
          percentage: "83%",
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
      margin: 2rem auto 0;
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
    padding: 6rem 0;
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
    }
  }
  .news {
    margin: 0 auto;
    text-align: center;
    padding-top: 6rem;
    .line {
      margin: 2rem auto 0;
    }
    .title {
      font-size: 3rem;
    }
    .card {
      width: 30%;
      margin: 5rem 3rem;
      line-height: 2rem;
      text-align: left;
      &__top {
        position: relative;
        img {
          width: 100%;
          margin-bottom: 1rem;
        }
        .tag {
          position: absolute;
          bottom: 15px;
          right: 15px;
          background-color: $bg-color-08;
          width: 45%;
          color: $txt-color-01;
          text-align: center;
          padding: 0.4rem;
          i {
            color: $txt-color-01;
          }
        }
      }
      .title {
        font-size: 1.6rem;
      }
      .text {
        font-size: 0.9rem;
      }
      .space {
        margin-right: 1.2rem;
      }
      i {
        color: $txt-color-08;
        margin-right: 0.6rem;
        font-size: 0.9rem;
      }
      p {
        &.text {
          font-size: 1.2rem;
          line-height: 2rem;
          padding: 0.5rem 0 1rem;
        }
      }
    }
  }
}
</style>
