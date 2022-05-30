<template>
  <div class="card">
    <img src="../assets/svg/svg-0.svg" alt="" />
    <div class="title">Knowing</div>
    <div class="text">
      Lorem, ipsum dolor sit amet consectetur adipisicing elit.
    </div>
  </div>
</template>

<script>
export default {
  name: "SpecCard",
};
</script>

<style lang="scss" scoped>
.card {
  padding-top: 5rem;
  line-height: 2rem;
  img {
    width: 50%;
  }
  .title {
    font-size: 1.5rem;
  }
  .text {
    font-size: 0.9rem;
  }
}
</style>
