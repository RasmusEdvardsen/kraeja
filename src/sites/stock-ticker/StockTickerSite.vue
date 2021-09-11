<script setup>
import { ref } from 'vue'
import axios from 'axios'
import StockTicker from './StockTicker.vue'

defineProps({
  msg: String
})

const getTicker = async (ticker) => {
  let token = 'c4t2beaad3icjlromfhg'
  let res = await axios.get(`https://finnhub.io/api/v1/quote?symbol=${ticker}&token=${token}`)
  return { name: ticker, data: res.data }
}

const ticker = ref("")
const tickers = ref([])
const addTicker = async () => tickers.value.push(await getTicker(ticker.value))
</script>

<template>
  <div class="container">
    <form class='stock-picker'>
      <input type="text" name="stock-ticker" id="stock-ticker" v-model="ticker">
      <button type="submit" @click.prevent="addTicker">Add +</button>
    </form>
    <ul class="stock-tickers">
      <StockTicker :ticker=ticker v-for="ticker in tickers" :key=ticker />
    </ul>
  </div>
</template>

<style scoped>
a {
  color: #42b983;
}
ul.stock-tickers {
  padding-inline-start: 0px;
}
</style>