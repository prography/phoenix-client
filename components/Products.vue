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
@import './assets/style/vars';

.grid {
  display: grid;
  margin: 16px 120px;
  grid-gap: 16px;
  grid-template-columns: repeat(4, calc((100% - 48px) / 4));

  @media #{$small-viweport} {
    margin: 16px;
    grid-template-columns: repeat(2, calc((100% - 16px) / 2));
  }
}
</style>
