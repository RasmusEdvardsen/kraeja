<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import HelloWorld from './sites/stock-ticker/StockTickerSite.vue'
import TopNav from './TopNav.vue'
</script>

<template>
  <div class="wrapper">
    <TopNav />
    <HelloWorld msg="Hello Vue 3 + Vite" />
  </div>
</template>

<style>
body {
  background-color: #f1f1f1;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
