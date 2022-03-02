<template>
  <agile  :autoplay-speed="2000" :autoplay="true" :slides-to-show="3">
    <div class="slide" v-for="(item, index) in product.gift" :key="index">
      <img :src="item.url" />
      <h3>{{ item.name }}</h3>
    </div>
  </agile>
</template>

<script>
import { VueAgile } from "vue-agile";
export default {
  name: "SliderCarousel",
  components: {
    agile: VueAgile,
  },
  data() {
    return {
      product: {
        gift: [
          {
            name: "三星蔥蛋捲",
            url: "https://www.june1.com.tw/assets/uploads/530x530/20210806160309242526.jpg",
          },
          {
            name: "咬咬果",
            url: "https://maruplayplay.com/wp-content/uploads/bitebitefruit1.jpg",
          },
          {
            name: "椰子球",
            url: "https://www.welcometw.com/wp-content/uploads/2020/05/%E5%9C%965-%E6%A4%B0%E5%AD%90%E7%90%83-mimima14-787x510-1.jpg",
          },
          {
            name: "三星蔥蛋捲",
            url: "https://www.june1.com.tw/assets/uploads/530x530/20210806160309242526.jpg",
          },
           {
            name: "咬咬果",
            url: "https://maruplayplay.com/wp-content/uploads/bitebitefruit1.jpg",
          },
          {
            name: "椰子球",
            url: "https://www.welcometw.com/wp-content/uploads/2020/05/%E5%9C%965-%E6%A4%B0%E5%AD%90%E7%90%83-mimima14-787x510-1.jpg",
          },
        ],
      },
     
    };
  },
};
</script>
<style scoped>
.slide {
  width: 100%;
  height: 100%;
  margin-top:10px;
}
.slide > img {
  height: 60vh;
}
</style>