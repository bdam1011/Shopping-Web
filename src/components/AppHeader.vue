<template>
  <header>
    <h1>{{ headerMessage }}</h1>
    <hr>
  </header>
</template>

<script>
    export default {
        name: "AppHeader",
        data() {
            return {
                headerMessage: "Hello! Vue.js"
            }
        }
    }
</script>