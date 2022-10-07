<template>
  <div class="pricing">
    <p style="font-size: 16px; margin-bottom: 15%">NT${{ pricing }}起</p>
  </div>
</template>

<script>
export default {
  name: "Pricing",
  props: {
    pricing: Number,
  },
};
</script>

<style scoped>
p {
  margin: 0px;
  padding: 2%;
}
</style>
