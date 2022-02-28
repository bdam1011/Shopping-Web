<template>
  <agile :prop="value">
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
        ],
      },
      value: {
        /**
         * Set the carousel to be the navigation of other carousels
         */
        asNavFor: {
          type: Array,
          default: function () {
            return [];
          },
        },
        /**
         * Enable autoplay
         */
        autoplay: {
          type: Boolean,
          default: false,
        },
        /**
         * Autoplay interval in milliseconds
         */
        autoplaySpeed: {
          type: Number,
          default: 3000,
        },
        /**
         * Enable centered view when slidesToShow > 1
         */
        centerMode: {
          type: Boolean,
          default: false,
        },
        /**
         * Slides padding in center mode
         */
        centerPadding: {
          type: String,
          default: "10%",
        },
        /**
         * Slide change delay in milliseconds
         */
        changeDelay: {
          type: Number,
          default: 0,
        },
        /**
         * Enable dot indicators/pagination
         */
        dots: {
          type: Boolean,
          default: true,
        },
        /**
         * Enable fade effect
         */
        fade: {
          type: Boolean,
          default: false,
        },
        /**
         * Infinite loop sliding
         */
        infinite: {
          type: Boolean,
          default: true,
        },
        /**
         * Index of slide to start on
         */
        initialSlide: {
          type: Number,
          default: 0,
        },
        /**
         * Enable mobile first calculation for responsive settings
         */
        mobileFirst: {
          type: Boolean,
          default: true,
        },
        /**
         * Enable prev/next navigation buttons
         */
        navButtons: {
          type: Boolean,
          default: true,
        },
        /**
         * All settings as one object
         */
        options: {
          type: Object,
          default: () => null,
        },
        /**
         * Pause autoplay when a dot is hovered
         */
        pauseOnDotsHover: {
          type: Boolean,
          default: false,
        },
        /**
         * Pause autoplay when a slide is hovered
         */
        pauseOnHover: {
          type: Boolean,
          default: true,
        },
        /**
         * Object containing breakpoints and settings objects
         */
        responsive: {
          type: Array,
          default: () => null,
        },
        /**
         * Enable right-to-left mode
         */
        rtl: {
          type: Boolean,
          default: false,
        },
        /**
         * Number of slides to scroll
         */
        slidesToScroll: {
          type: Number,
          default: 1,
        },
        /**
         * Number of slides to show
         */
        slidesToShow: {
          type: Number,
          default: 1,
        },
        /**
         * Slide animation speed in milliseconds
         */
        speed: {
          type: Number,
          default: 300,
        },
        /**
         * Swipe distance
         */
        swipeDistance: {
          type: Number,
          default: 50,
        },
        /**
         * Throttle delay in milliseconds
         */
        throttleDelay: {
          type: Number,
          default: 500,
        },
        /**
         * Transition timing function
         * Available: ease, linear, ease-in, ease-out, ease-in-out
         */
        timing: {
          type: String,
          default: "ease",
          validator: (value) => {
            return (
              ["ease", "linear", "ease-in", "ease-out", "ease-in-out"].indexOf(
                value
              ) !== -1
            );
          },
        },
        /**
         * Disable Agile carousel
         */
        unagile: {
          type: Boolean,
          default: false,
        },
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