<template>
  <header>
    <h1>{{ headerMessage }}</h1>
    <hr>
    <h1>hi</h1>
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