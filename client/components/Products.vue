<template>
  <div class="grid">
    <ProductCard v-for="item in items" :key="item.index" :title="item.text"/>
  </div>
</template>

<script>
import ProductCard from '@/components/ProductCard.vue'

export default {
  name: 'Products',
  components: {
    ProductCard
  },
  props: {
    items: Array
  }
}
</script>

<style lang="scss" scoped>
.grid {
  display: grid;
  margin: 1rem calc(6em + 24px);
  grid-gap: 1rem;
  grid-template-columns: repeat(4, calc((100% - 3rem) / 4));
}
</style>
