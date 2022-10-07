<template>
  <header>
    <h1>Hotel Web App</h1>
  </header>
  <main>
    <div class="filter">
      <div>透過以下分類搜尋:</div>
      <div>
        <h3>飯店設施</h3>
        <i class="bi bi-caret-down"></i>
        <input type="checkbox" value="免費無線網路" />
        <label>免費無線網路</label><br />
        <input type="checkbox" value="禁菸客房" />
        <label>禁菸客房</label><br />
        <input type="checkbox" value="廚房" />
        <label>廚房</label><br />
        <input type="checkbox" value="洗衣房" />
        <label>洗衣房</label><br />
        <input type="checkbox" value="停車場" />
        <label>停車場</label><br />
        <input type="checkbox" value="寵物友善" />
        <label>寵物友善</label><br />
      </div>
    </div>
    <div class="content">
      <p class="search_result">找到 {{ reviews.length + 1 }} 間住宿</p>
      <div :key="review.id" v-for="review in reviews">
        <!-- <p>{{ review.id }}</p> -->
        <Review :review="review" />
      </div>
      <!-- <Review :review="reviews[0]" /> -->
      <!-- <Review :review="reviews[1]" /> -->
    </div>
  </main>
</template>

<script>
import Review from "./components/Review.vue";

export default {
  name: "App",
  components: {
    Review,
  },
  props: {
    reviews: Array,
  },
  data() {
    return {
      reviews: [],
    };
  },
  created() {
    this.reviews = [
      // https://www.booking.com/landmark/tw/taipei-city-government.zh-tw.html
      {
        id: 1,
        title: "台北W酒店",
        location: "台北市",
        description:
          "台北 W 飯店兼具藝術與時尚元素，提供奢華住宿體驗，坐落在信義區中心地帶。飯店位於統一時代百貨台北店正上方，擁有美麗的 WET® 室外游泳池和時尚的 Woobar 酒...",
        rating: 8.7,
        pricing: 7875,
        // src: "./assets/Image/W_hotel.png",
        src: "https://cf.bstatic.com/xdata/images/hotel/max1024x768/22359134.jpg?k=92578a7877e65c7afb275bbd5be9601ef472c53bcf96dcc1632e8291cebb2e58&o=&hp=1",
      },
      {
        id: 2,
        title: "寒舍艾麗酒店",
        location: "台北市",
        description:
          "寒舍艾麗酒店位於台北市信義區，客房空間寬敞，採現代風格，提供免費 WiFi。飯店附設健身中心和餐廳。 寒舍艾麗酒店距離捷運市政府站和台北 101 步行 5 分鐘。步行...",
        rating: 8.6,
        pricing: 4966,
        // src: "./assets/Image/alley_hotel.png",
        src: "https://cf.bstatic.com/xdata/images/hotel/max1024x768/23833190.jpg?k=60a2a0ea656a35f6203ec73bce060631bf820433877eca8cbcd790e45c0bc58b&o=&hp=1",
      },
      {
        id: 3,
        title: "誠品行旅",
        location: "台北市",
        description:
          "誠品行旅位於松山文創園區，距離捷運國父紀念館站步行僅 10 分鐘，設有最先進的健身中心、寬敞的宴會廳和豪華客房。 飯店距離台北松山機場僅 10 分鐘車程；距離台北車站 15 分鐘車程；距離松山車站 10 分鐘車程；距離...",
        rating: 9.2,
        pricing: 5687,
        // src: "./assets/Image/elite_hotel.png",
        src: "https://cf.bstatic.com/xdata/images/hotel/max1024x768/199396927.jpg?k=5646327fd5f9c59a03f6b77adb777fe4607f1e00449c00914353af07096366f9&o=&hp=1",
      },
      {
        id: 4,
        title: "正旅館 (信義)",
        location: "台北市",
        description:
          "Just Inn Taipei (Xin Yi) 地點很方便，位於台北的信義區，距離台北 101 1.3 公里，距離通化夜市 1.9 公里，距離饒河街觀光夜市 1.5 公里。這間住宿提供的設施與服務包...",
        rating: 8.3,
        pricing: 1309,
        // src: "./assets/Image/just_inn.png",
        src: "https://cf.bstatic.com/xdata/images/hotel/max1024x768/125323743.jpg?k=d735f84cb62e91cc5ce2d7cf382271ffd9b420c7d1b0dad98aba696008f9e6c1&o=&hp=1",
      },
      {
        id: 5,
        title: "莯旅 MOOD Inn",
        location: "台北市",
        description:
          "莯旅 MOOD Inn 位在台北，距離饒河街觀光夜市 1.7 公里，有附 WiFi(免費)的空調客房和快速辦理入住/退房服務。這間住宿距離五分埔成衣批发区 1.8 公里，距離台...",
        rating: 7.9,
        pricing: 1180,
        // src: "./assets/Image/mood_inn.png",
        src: "https://cf.bstatic.com/xdata/images/hotel/max1024x768/320722704.jpg?k=a5c443740674c9139a5a7cb369ce6ed0a2e06333e8fccb29adab9b5d995587cc&o=&hp=1",
      },
    ];
  },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
h1 {
  margin-left: 2%;
}
main {
  display: flex;
}

.search_result {
  padding-left: 2%;
  margin: 0px;
}
.filter {
  /* background-color: rgb(250, 154, 154); */
  height: 100vh;
  min-width: 150px;
  flex-grow: 1;
  padding: 1%;
}

.content {
  display: flex;
  flex-grow: 3;
  flex-direction: column;
  padding: 1%;
  max-height: 200px;
}
</style>
