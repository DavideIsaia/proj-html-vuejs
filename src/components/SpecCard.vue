<template>
  <div class="card">
    <img
      :src="require(`../assets/svg/${element.thumb}`)"
      :alt="element.title"
    />
    <div class="title">{{ element.title }}</div>
    <div class="text">{{ element.text }}</div>
  </div>
</template>

<script>
export default {
  name: "SpecCard",
  props: {
    element: Object,
  },
};
</script>

<style lang="scss" scoped>
.card {
  padding-top: 5rem;
  line-height: 2rem;
  img {
    width: 50%;
    margin-bottom: 1rem;
  }
  .title {
    font-size: 1.5rem;
  }
  .text {
    font-size: 1rem;
  }
}
</style>
