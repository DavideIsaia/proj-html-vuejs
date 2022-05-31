<template>
  <div class="meeting clearfix">
    <div class="date">
      <div class="day">{{ element.day }}</div>
      <div class="month">{{ element.month }}</div>
    </div>
    <div class="col-right">
      <h6>{{ element.title }}</h6>
      <div>
        <i class="far fa-clock"></i><span class="text">{{ element.hour }}</span>
      </div>
      <div>
        <i class="fas fa-map-marker-alt"></i
        ><span class="text">{{ element.place }}</span>
      </div>
      <div class="read-more">read more</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CalendarCard",
  props: {
    element: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
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
</style>
