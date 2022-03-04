<template>
  <div>
  
      <select v-model="place">
        <option disabled value="">請選擇</option>
        <option v-for="item in counties" :key="item">{{item}}</option>
      </select>
      <input type="text" v-model="souvenir" placeholder="souvenir" />
      <button type="submit" @click="search()">搜尋</button>
 
  </div>
</template>

<script>
export default {
  name: "SearchBox",
  data() {
    return {
      place: "",
      souvenir: "",
      counties: [
        '台北市', '基隆市', '新北市', '宜蘭縣', '桃園市', '新竹市', '新竹縣', '苗栗縣',
        '台中市', '彰化縣', '南投縣', '嘉義市', '嘉義縣', '雲林縣', '台南市', '高雄市',
        '澎湖縣', '金門縣', '屏東縣', '台東縣', '花蓮縣', '連江縣'
    ],
    };
  },
  methods: {
    search() {
      console.log(this.place+this.souvenir);
      this.$router.push({ name: "shopcartr" });
    },
  },
};
</script>
<style scoped>
div{

  position: absolute;
  right: 0px;
}
div input{
  width: 40vw;
} 
</style>