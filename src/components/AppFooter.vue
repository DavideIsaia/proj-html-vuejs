<template>
  <footer>
    <div class="container clearfix">
      <!-- colonna abiut -->
      <div class="left">
        <h4 class="title">About</h4>
        <div class="line"></div>
        <p class="text">
          We created Everlead to effectively become the stepping stone torwards
          meeting all your goals &#38; achievinf business success.
        </p>
        <div class="social">
          <i class="fab fa-linkedin-in"></i>
          <i class="fab fa-facebook-f"></i>
          <i class="fab fa-twitter"></i>
        </div>
      </div>
      <!-- colonna twitter -->
      <div class="left">
        <h4 class="title">Twitter</h4>
        <div class="line"></div>
        <div class="flex">
          <i class="fab fa-twitter"></i>
          <p class="text">
            <a href="">@aliasadadm</a> Hi <a href="">@aliasadadm</a>, can you
            <a href="">https://t.co/JLV61aXG7d</a> and one of our please submit
            a ticket at support agent...
            <a href="">https://t.co/yk57k159bs</a>
          </p>
        </div>
        <div class="flex">
          <i class="fab fa-twitter"></i>
          <p class="text">
            <a href="">@HenrySefaBoakyl</a> Check out our theme Gioia which has
            all necessary elements to build a multi vendor marketplace.
            <a href="">https://t.co/c9BIYxZBIL</a>
          </p>
        </div>
      </div>
      <!-- colonna links -->
      <div class="left">
        <h4 class="title">Important links</h4>
        <div class="line"></div>
        <!-- link footer dinamici -->
        <ul>
          <li v-for="item in links" :key="item" class="links">
            <a href="" class="text">{{ item }}</a>
          </li>
        </ul>
      </div>
      <!-- colonna contact -->
      <div class="right">
        <h4 class="title">Contact me</h4>
        <div class="line"></div>
        <div class="flex">
          <i class="fas fa-map-marker-alt"></i>
          <p class="text">457 BigBlue Street, NY 10013</p>
        </div>
        <div class="flex">
          <i class="fas fa-phone"></i>
          <p class="text">(315) 5512-2579</p>
        </div>
        <div class="flex">
          <i class="fas fa-envelope"></i>
          <p class="text">everlead@mikado.com</p>
        </div>
        <!-- subscribe form -->
        <input type="text" class="text" id="name" placeholder="Your Name" />
        <button class="sub">Subscribe</button>
      </div>
    </div>
    <div class="copyright text">CopyrightEverlead&copy;MikadoThemes</div>
  </footer>
</template>

<script>
export default {
  name: "AppFooter",
  data() {
    return {
      links: [
        "About me",
        "About us",
        "Language packs",
        "Become a coach",
        "Monthly Events",
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
footer {
  background-color: $bg-color-15;
  .container {
    padding: 8rem 0;
  }
  .title {
    color: $txt-color-01;
    font-size: 1.2rem;
  }
  .line {
    width: 2rem;
    margin: 1rem 0;
  }
  .text {
    font-size: 0.9rem;
    color: $txt-color-07;
    line-height: 1.5rem;
  }
  .left {
    width: 22%;
    padding-right: 2.5rem;
    .social i {
      background-color: $bg-color-01;
      color: $txt-color-13;
      margin-top: 2rem;
      &:hover {
        color: $txt-color-01;
        background-color: $bg-color-08;
      }
    }
    .links {
      line-height: 1.8rem;
      a:hover {
        color: $txt-color-08;
      }
    }
    .flex {
      padding-bottom: 1rem;
      a {
        text-decoration: underline;
        &:hover {
          color: $txt-color-08;
        }
      }
      i {
        color: $txt-color-08;
        align-self: flex-start;
        padding: 0.5rem 1.2rem 0 0;
        font-size: 1.1rem;
      }
    }
  }
  .right {
    position: relative;
    min-width: 25%;
    .flex {
      justify-content: flex-start;
    }
    i {
      color: $txt-color-08;
      padding-right: 1.2rem;
    }
    p {
      line-height: 2rem;
    }
    input {
      border: 0;
      border-bottom: 2px solid $bdr-color-04;
      background-color: $bg-color-15;
      min-width: 100%;
      font-size: 0.9rem;
      margin-top: 3rem;
      padding: 0.3rem 0;
    }
    .sub {
      position: absolute;
      bottom: -25px;
      right: 0;
      padding: 0;
      background-color: $bg-color-15;
      color: $txt-color-03;
      &:hover {
        color: $txt-color-08;
      }
    }
  }
}
.copyright {
  background-color: $bg-color-08;
  padding: 0.4rem;
  text-align: center;
  font-size: 0.9rem;
  &.text {
    color: $txt-color-01;
  }
}
</style>
