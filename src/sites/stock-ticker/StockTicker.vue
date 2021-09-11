<template>
  <div class="stock-ticker">
      {{ ticker.name }} {{ ticker.data }}
  </div>
</template>

<script setup>
defineProps({
    ticker: Object
})
</script>

<style scoped>
.stock-ticker {
  background-color: white;
  border: 1px solid gray;
  border-radius: 4px;

  padding:8px;
  margin: 8px 0;
}
</style>