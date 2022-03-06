<template>
  <div class="all">
    <div class="userData">
      <user-data />
    </div>
    <div class="tradeInfo">
      <scroll-table />
    </div>
  </div>
</template>
<script>
import UserData from "@/components/UserData.vue";
import ScrollTable from "@/components/ScrollTable.vue";
export default {
  components: {
    UserData,
    ScrollTable,
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