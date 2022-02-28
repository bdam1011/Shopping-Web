<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <slider-carousel/>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue';
import SliderCarousel from "@/components/Slider.vue";

export default {
  name: 'HomeView',
  components: {
    HelloWorld,
    SliderCarousel
  }
}
</script>
