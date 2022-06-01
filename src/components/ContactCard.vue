<template>
  <section class="contact">
    <div class="container clearfix">
      <div class="left">
        <div class="dots">
          <img src="../assets/img/h1-contact-rev-02.png" alt="" />
          <img src="../assets/img/h1-contact-rev-02.png" alt="" />
          <img src="../assets/img/h1-contact-rev-02.png" alt="" />
        </div>
        <div class="label">
          <img src="../assets/img/h1-contact-rev-03.png" alt="" />
          <span class="title bold">New York Coaching</span>
          <span class="read-more">read more</span>
        </div>
      </div>
      <div class="right">
        <h3 class="title bold">Contact us<span>.</span></h3>
        <div class="text">
          Lorem ipsum, dolor sit amet consectetur adipisicing elit
        </div>
        <div class="line"></div>
        <input
          type="text"
          class="control text"
          id="name"
          placeholder="Your Name"
        />
        <input
          type="email"
          class="control text"
          id="email"
          placeholder="Your Email"
        />
        <textarea
          class="control text"
          placeholder="Write a message..."
        ></textarea>
        <button class="orange">
          <span>Send</span
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
      <!-- icone degli sponsor aggiunte dinamicamente -->
      <div class="sponsor flex">
        <div v-for="item in logos" :key="item" class="wrapper">
          <img
            :src="require(`../assets/img/h4-clients-img-${item.img}.png`)"
            alt=""
          />
          <img
            class="hide"
            :src="require(`../assets/img/h4-clients-img-${item.hide}.png`)"
            alt=""
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ContactCard",
  data() {
    return {
      logos: [
        {
          img: "03",
          hide: "04-1",
        },
        {
          img: "05",
          hide: "06-1",
        },
        {
          img: "07",
          hide: "08-1",
        },
        {
          img: "09",
          hide: "10-1",
        },
        {
          img: "01",
          hide: "02",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
.contact {
  margin-top: 8rem;
  background-color: $bg-color-04;
  .left {
    width: 45%;
    background-image: url("../assets/img/h1-contact-rev-01.png");
    background-size: contain;
    background-repeat: no-repeat;
    height: 400px;
    .dots {
      position: relative;
      cursor: pointer;
      img {
        position: absolute;
        width: 5%;
      }
      :first-child {
        top: 130px;
        left: 160px;
      }
      :nth-child(2) {
        top: 100px;
        left: 300px;
      }
      :last-child {
        top: 250px;
        right: 90px;
      }
    }
    .label {
      position: relative;
      img {
        width: 40%;
        position: absolute;
        top: 170px;
        left: 160px;
      }
      :nth-child(2) {
        position: absolute;
        top: 190px;
        left: 190px;
        font-size: 1.1rem;
      }
      :last-child {
        position: absolute;
        top: 230px;
        left: 190px;
        font-size: 0.8rem;
      }
    }
  }
  .right {
    width: 45%;
    h3 {
      font-size: 3rem;
    }
    .control {
      border: 0;
      border-bottom: 2px solid $bdr-color-04;
      background-color: $bg-color-04;
      font-size: 0.9rem;
      padding: 1rem;
    }
    #name {
      margin-right: 3.3rem;
    }
    input {
      min-width: 45%;
    }
    textarea {
      display: block;
      min-height: 100px;
      min-width: 100%;
    }
    .orange {
      background-color: $bg-color-08;
      color: $txt-color-01;
      margin: 2rem 0;
      padding: 0.8rem 1.5rem;
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
  .sponsor {
    width: 100%;
    float: left;
    .wrapper {
      position: relative;
      width: calc(100% / 5);
      height: 250px;
      &:hover {
        .hide {
          display: block;
          cursor: pointer;
        }
      }
    }
    .hide {
      display: none;
    }
    img {
      position: absolute;
      top: 0;
      left: 0;
      padding: 5rem;
    }
  }
}
</style>
