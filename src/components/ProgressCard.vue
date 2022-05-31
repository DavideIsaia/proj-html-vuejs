<template>
  <div class="bar-container clearfix">
    <h5 class="title bold left">{{ element.title }}</h5>
    <h5 class="title bold right">{{ element.percentage }}</h5>
    <div class="progress-bar">
      <div class="filled" :style="{ width: element.percentage }"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProgressCard",
  props: {
    element: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
.bar-container {
  padding-bottom: 2rem;
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
    height: 3px;
    background-color: $bg-color-08;
  }
}
</style>
