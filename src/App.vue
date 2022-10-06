
<template>
  <header>
    <h1>Hotel Web App</h1>
  </header>
  <main>
    <div class="filter">

    </div>
    <div class="content">
      <!-- <div :key="review.id" v-for="review in reviews"> -->
        <!-- <p>{{review.id}}</p> -->
        <!-- <Review review={{review}} /> -->
      <!-- </div> -->
      <Review :review="reviews[0]" />
      <!-- <Review :review="reviews[1]" /> -->
    </div>
  </main>
</template>

<script>
import Review from "./components/Review.vue"

export default {
  name: "App",
  components: {
    Review,
  },
  props: {
    reviews: Array
  },
  data() {
    return {
      reviews: []
    }
  },
    created() {
      this.reviews = [
        // https://www.booking.com/landmark/tw/taipei-city-government.zh-tw.html
        {
          id: 1,
          title: "台北W酒店",
          location: "台北市",
          description: "台北 W 飯店兼具藝術與時尚元素，提供奢華住宿體驗，坐落在信義區中心地帶。飯店位於統一時代百貨台北店正上方，擁有美麗的 WET® 室外游泳池和時尚的 Woobar 酒...",
          rating: 8.7,
          pricing: 7875,
          src: "./assets/Image/W_hotel.png"
          // src: "https://www.booking.com/hotel/tw/w-taipei.zh-tw.html?label=gen173nr-1FCAUo5wFCFnRhaXBlaS1jaXR5LWdvdmVybm1lbnRIMFgEaOcBiAEBmAEwuAEXyAEP2AEB6AEB-AECiAIBqAIDuAKW0fqZBsACAdICJGY1NGU5MzBmLTRhMzMtNGU3ZC1hNmYwLTBmNWI4NGRiOTkzN9gCBeACAQ&sid=720bb1ab2367d2a46773a5df3b501c9a"
        },
        {
          id: 2,
          title: "寒舍艾麗酒店",
          location: "台北市",
          description: "寒舍艾麗酒店位於台北市信義區，客房空間寬敞，採現代風格，提供免費 WiFi。飯店附設健身中心和餐廳。 寒舍艾麗酒店距離捷運市政府站和台北 101 步行 5 分鐘。步行...",
          rating: 8.6,
          pricing: 4966,
          src: "./assets/Image/alley_hotel.png"
        },
        {
          id: 3,
          title: "誠品行旅",
          location: "台北市",
          description: "誠品行旅位於松山文創園區，距離捷運國父紀念館站步行僅 10 分鐘，設有最先進的健身中心、寬敞的宴會廳和豪華客房。 飯店距離台北松山機場僅 10 分鐘車程；距離台北車站 15 分鐘車程；距離松山車站 10 分鐘車程；距離...",
          rating: 9.2,
          pricing: 5687,
          src: "./assets/Image/elite_hotel.png"
        },
        {
          id: 4,
          title: "正旅館 (信義)",
          location: "台北市",
          description: "Just Inn Taipei (Xin Yi) 地點很方便，位於台北的信義區，距離台北 101 1.3 公里，距離通化夜市 1.9 公里，距離饒河街觀光夜市 1.5 公里。這間住宿提供的設施與服務包...",
          rating: 8.3,
          pricing: 1309,
          src: "./assets/Image/just_inn.png"
        },
        {
          id: 5,
          title: "莯旅 MOOD Inn",
          location: "台北市",
          description: "莯旅 MOOD Inn 位在台北，距離饒河街觀光夜市 1.7 公里，有附 WiFi(免費)的空調客房和快速辦理入住/退房服務。這間住宿距離五分埔成衣批发区 1.8 公里，距離台...",
          rating: 7.9,
          pricing: 1180,
          src: "./assets/Image/mood_inn.png"
        },
      ]
  }
};
</script>

<style scoped>
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
  }
  
  main {
    display: flex;
  }

  .filter {
    background-color: grey;
    height: 100vh;
    flex-grow: 1;
    margin: 10px;
  }

  .content {
    display: flex;
    flex-direction: column;
    flex-grow: 4;
  }
</style>
