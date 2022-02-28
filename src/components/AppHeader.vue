<template>
    <nav>
      <ul class="router-inlineblock">
        <li><router-link to="/">Home</router-link></li>
        <li><router-link to="/about">About</router-link></li>
      </ul>
    </nav>
</template>

<script>
export default {
  name: "AppHeader",
  data() {
    return {
      headerMessage: "Hello! Vue.js",
    };
  },
};
</script>

<style scoped>

nav > ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  /* overflow: hidden; */
  background-color: #38444d;
}

.router-inlineblock>li{
  display: inline-block;
  text-align: justify;
  padding: 10px 40px;
}


nav li:hover {
    background-color: rgb(115, 115, 115);
    color: white;
}

nav a {
  color: white;
  display: block; /* 讓 <a> 填滿 <li> */
  font-size: 1.5rem;
  text-decoration: none;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>