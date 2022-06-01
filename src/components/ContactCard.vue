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
        <button class="orange">Send</button>
      </div>
      <div class="sponsor flex">
        <div class="wrapper">
          <img src="../assets/img/h4-clients-img-03.png" alt="" />
          <img
            class="hide"
            src="../assets/img/h4-clients-img-04-1.png"
            alt=""
          />
        </div>
        <div class="wrapper">
          <img src="../assets/img/h4-clients-img-03.png" alt="" />
          <img
            class="hide"
            src="../assets/img/h4-clients-img-04-1.png"
            alt=""
          />
        </div>
        <div class="wrapper">
          <img src="../assets/img/h4-clients-img-03.png" alt="" />
          <img
            class="hide"
            src="../assets/img/h4-clients-img-04-1.png"
            alt=""
          />
        </div>
        <div class="wrapper">
          <img src="../assets/img/h4-clients-img-03.png" alt="" />
          <img
            class="hide"
            src="../assets/img/h4-clients-img-04-1.png"
            alt=""
          />
        </div>
        <div class="wrapper">
          <img src="../assets/img/h4-clients-img-03.png" alt="" />
          <img
            class="hide"
            src="../assets/img/h4-clients-img-04-1.png"
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
