<template>
  <agile :prop="value">
    <div class="slide">
      <h3>slide 1</h3>
    </div>
    <div class="slide">
      <h3>slide 2</h3>
    </div>
    <div class="slide">
      <h3>slide 3</h3>
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
      prop: {
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
          default: "15%",
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