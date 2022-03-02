<template>
  <ul class="router-inlineblock">
    <li><router-link to="/about">免責聲明</router-link></li>
    <li><router-link to="/about">關於我們</router-link></li>
    <li><router-link to="/about">常見問題</router-link></li>
  </ul>
</template>
<script>
export default {
  name: "AppFooter",
};
</script>
<style scoped>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  /* overflow: hidden; */
  background-color: #38444d;
}
.router-inlineblock>li{
  display: inline-block;
  text-align: justify;
  padding: 10px 5%;
}
li:hover {
    background-color: rgb(115, 115, 115);
    color: white;
}
a {
  color: white;
  display: block; /* 讓 <a> 填滿 <li> */
  font-size: 1.5rem;
  text-decoration: none;
}

a.router-link-exact-active {
  color: #42b983;
}
</style>