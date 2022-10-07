<template>
  <div>
    <img src="../assets/location-dot-solid.svg" alt="location-dot-solid" />{{
      location
    }}
  </div>
</template>

<script>
export default {
  name: "Location",
  props: {
    location: String,
  },
};
</script>

<style scoped>
div {
  display: flex;
}
img {
  max-width: 12px;
  margin-right: 3px;
}
</style>
