<template>
  <app-header/>
  <slider-carousel/>
  <!-- <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav> -->
 <router-view/>
</template>

<script>
import AppHeader from "@/components/AppHeader.vue";
import SliderCarousel from "@/components/Slider.vue"

export default {
  name: "App",
  components: {
    AppHeader,
    SliderCarousel
  },
};
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

/* nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
} */
</style>
