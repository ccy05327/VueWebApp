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
  <!-- <p class="search_result">找到 6 間住宿</p> -->
  <div class="review">
    <!-- Take the input whole review, use the property for each -->
    <div class="hotel_image">
      <Image :source="review.src" :title="review.title" />
    </div>

    <div class="hotel_content">
      <div class="hotel_title">
        <Title :title="review.title" />
      </div>

      <div class="hotel_location">
        <Location :location="review.location" />
      </div>
      <div class="hotel_description">
        <Description :description="review.description" />
      </div>
    </div>
    <div class="hotel_other">
      <div class="hotel_rating">
        <Rating :rating="review.rating" />
      </div>
      <div class="hotel_pricing">
        <Pricing :pricing="review.pricing" />
      </div>
    </div>
  </div>
</template>

<style scoped>
h2,
h3,
h4 {
  margin: 0px;
}

.review {
  /* height: 100vh; */
  flex-grow: 2;
  /* background-color: white; */
  display: flex;
  padding: 1%;
}

.hotel_image {
  flex-grow: 2;
  /* height: 150px; */
  /* min-width: 150px; */
  /* background-color: grey; */
}

.hotel_content {
  /* height: 150px; */
  flex-grow: 3;
  display: flex;
  flex-direction: column;
  margin-left: 10px;
}
.hotel_title {
  /* background-color: rgb(123, 177, 239); */
  padding: 1%;
}

.hotel_location {
  /* background-color: rgb(194, 139, 246); */
  padding: 1%;
}

.hotel_description {
  /* background-color: rgb(105, 224, 228); */
  padding-left: 1%;
  padding-right: 5%;
}

.hotel_other {
  /* height: 150px; */
  /* background-color: grey; */
  flex-grow: 2;
  min-width: 100px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.hotel_rating {
  margin: auto;
}

.hotel_pricing {
  padding: 1%;
  font-size: 14px;
}
</style>
