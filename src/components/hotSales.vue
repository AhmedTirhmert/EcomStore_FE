<template>
  <div class="hot-sales">
    <h2 class="hot-sales-title">Hot Sales</h2>
    <div class="hot-sales-cards">
      <product-card v-for="i in 4" :key="i" />
    </div>
  </div>
</template>

<script>
export default {
  name: "HotSales",
  components: {
    ProductCard: () => import("@/components/product/ProductCard.vue"),
  },
};
</script>

<style scoped>
.hot-sales {
  margin: 2em;
}
.hot-sales-title {
  font-family: "Merriweather Sans";
  text-align: start;
  letter-spacing: 0.1em;
  padding-left: 0.5em;
  position: relative;
}
.hot-sales-title::after {
  content: "";
  position: absolute;
  background-color: rgba(0, 0, 0, 0.7);
  width: 9%;
  height: 3px;
  left: 12px;
  bottom: 0;
}
.hot-sales-cards {
  display: flex;
  justify-content: space-between;
  overflow-x: auto;
  padding: 1.5em 2em;
  z-index: 1;
}
.hot-sales-cards::-webkit-scrollbar {
  height: 5px;
}

.hot-sales-cards::-webkit-scrollbar-track {
  box-shadow: orange;
  border-radius: 10px;
}

.hot-sales-cards::-webkit-scrollbar-thumb {
  border-radius: 10px;
  background-color: #606060;
}
</style>