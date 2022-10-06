<template>
  <img src={{source}} alt={{title}} />
  <h3>{{title}}</h3>
</template>

<script>
export default {
  name: "Image",
  props: {
    source: String,
    title: String,
  },
};
</script>

<style>
image {
  max-width: 150px;
}
</style>
