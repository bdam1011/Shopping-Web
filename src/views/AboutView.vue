<template>
  <div class="about">
    <h1>This is an about page</h1>
    <AppHeader/>
  </div>
</template>
<script>
import AppHeader from "@/components/AppHeader.vue";

export default {
  name: "AboutView",
  components: {
    AppHeader,
  },
};
</script>