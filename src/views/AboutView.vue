<template>
  <div class="about">
    <h1>This is an about page</h1>
    <user-data/>
  </div>
</template>
<script>
import UserData from '@/components/UserData.vue';
export default {
  components: {
    UserData,
  }
}
</script>
