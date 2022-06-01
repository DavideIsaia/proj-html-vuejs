<template>
  <section class="news">
    <div class="container">
      <h3 class="title bold">Latest News<span>.</span></h3>
      <p class="text">
        Lorem, ipsum dolor sit amet consectetur adipisicing elit
      </p>
      <img class="svg" src="../assets/svg/svg-4.svg" alt="" />
      <div class="line"></div>
      <div class="flex">
        <div v-for="item in newsArray" :key="item" class="card">
          <div class="card__top">
            <img
              :src="require(`../assets/img/h1-blog-img-${item.img}.jpg`)"
              :alt="item.title"
            />
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
          <h5 class="title bold">{{ item.title }}</h5>
          <p class="text">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Alias
            tenetur...
          </p>
          <div class="read-more">read more</div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "NewsCard",
  data() {
    return {
      newsArray: [
        {
          title: "Next Investment",
          img: "02",
        },
        {
          title: "Team Building",
          img: "03",
        },
        {
          title: "New Business Day",
          img: "01",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
.news {
  position: relative;
  margin: 0 auto;
  text-align: center;
  padding-top: 6rem;
  .svg {
    width: 20%;
    position: absolute;
    top: -4rem;
    left: 15rem;
  }
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
</style>
