<script>
import Image from "./Image.vue";
import Title from "./Title.vue";
import Location from "./Location.vue";
import Description from "./Description.vue";
import Rating from "./Rating.vue";
import Pricing from "./Pricing.vue";

export default {
  name: "Review",
  components: {
    Image,
    Title,
    Location,
    Description,
    Rating,
    Pricing,
  },
  props: {
    review: Object,
  },
};
</script>

<template>
  <div class="review">
    <!-- Take the input whole review, use the property for each -->
    <div class="hotel_image">
      <!-- Input the source file -->
      <div>{{review.title}}</div>
      <Image :source="review.src" :title="review.title" />
    </div>

    <div class="hotel_content">
      <div class="hotel_title">
        <!-- Input review.title -->
        <!-- <Title review.title/> -->
      </div>

      <div class="hotel_location"></div>
      <!-- Input review.location -->
      <!-- <Location review.location/> -->
      <div class="hotel_description"></div>
      <!-- Input review.description -->
      <!-- <Description review.description /> -->
    </div>
    <div class="hotel_other">
      <div class="hotel_rating"></div>
      <!-- Input review.rating -->
      <!-- <Rating review.rating /> -->
      <div class="hotel_pricing"></div>
      <!-- Input review.pricing -->
      <!-- <Pricing review.pricing /> -->
    </div>
  </div>
</template>

<style scoped>
.review {
  height: 100vh;
  flex-grow: 3;
  background-color: white;
  display: flex;
  margin: 10px;
  /* border-radius: 10px; */
}

.hotel_image {
  flex-grow: 2;
  height: 150px;
  background-color: grey;
}

.hotel_content {
  height: 150px;
  flex-grow: 4;
  display: flex;
  flex-direction: column;
  margin: 5px;
  border-radius: 5px;
}
.hotel_title {
  flex-grow: 1;
  margin: 5px;
  background-color: grey;
}

.hotel_location {
  flex-grow: 1;
  background-color: grey;
  margin: 5px;
}

.hotel_description {
  flex-grow: 4;
  background-color: grey;
  margin: 5px;
}

.hotel_other {
  height: 150px;
  background-color: grey;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.hotel_rating {
}

.hotel_pricing {
}
</style>
