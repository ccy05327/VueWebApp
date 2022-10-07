<template>
  <div>
    <img :src=source alt="{{title}}" />
  </div>
</template>

<script>
export default {
  name: "Image",
  props: {
    source: String,
    title: String,
  },
  data() {
    return {
    //   source: require(this.source),
    };
  },
};
</script>

<style scoped>
img {
  width: 200px;
  height: 160px;
}
</style>
