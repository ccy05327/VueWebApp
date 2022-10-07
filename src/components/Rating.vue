<template>
  <div>
    <button>{{ rating }}</button>
    <div>{{ level }}</div>
  </div>
</template>

<script>
export default {
  name: "Rating",
  props: {
    rating: Number,
    level: String,
  },
  //   data() {
  //     let level;
  //     if (this.rating >= 9.0 && this.rating <= 10.0) {
  //       level = "好極了";
  //     } else if (this.rating >= 8.5 && this.rating < 9.0) {
  //       level = "很棒";
  //     } else if (this.rating >= 8.0 && this.rating < 8.5) {
  //       level = "非常好";
  //     } else if (this.rating >= 7.0 && this.rating < 8.0) {
  //       level = "好";
  //     } else {
  //       level = "評分";
  //     }
  //     return level;
  //   },
};
</script>

<style>
button {
  min-width: 30px;
  min-height: 30px;
  width: 4vw;
  height: 4vw;
  font-size: 1.5rem;
}
</style>
