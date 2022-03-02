<template>
  <div class="home">
    <search-box/>
    <slider-carousel/>
    <HelloWorld msg="Welcome to Souvenir Shop of Agricultural Products "/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue';
import SliderCarousel from "@/components/Slider.vue";
import SearchBox from "@/components/SearchBox.vue";

export default {
  name: 'HomeView',
  components: {
    HelloWorld,
    SliderCarousel,
    SearchBox
  }
}
</script>
