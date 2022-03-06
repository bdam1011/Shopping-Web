<template>
  <div class="all">
    <div class="userData">
      <user-data />
    </div>
    <div class="tradeInfo">
      <router-link to="/userpage">商品庫存</router-link>
      <router-link to="/userpage/scrolltable2">出貨狀況</router-link>
      <router-view></router-view>
      <!-- <scroll-table /> -->
    </div>
  </div>
</template>
<script>
import UserData from "@/components/UserData.vue";
// import ScrollTable from "@/components/ScrollTable.vue";
export default {
  components: {
    UserData,
    // ScrollTable,
  },
};
</script>
<style scoped>
.all{
  display: flex;
}
.userData{
  align-items: center;
  width: 20vw;
  padding: 20px;
}
.tradeInfo{
  align-items: center;
  width: 80vw;
  padding: 20px;
}
</style>