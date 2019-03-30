<template>
  <main>
    <Header/>
    <Products :items="products"/>
    <Footer/>
  </main>
</template>

<script>
import Footer from '@/components/Footer.vue'
import Header from '@/components/Header.vue'
import Products from '@/components/Products.vue'

import products from '@/assets/data/tempProducts'

export default {
  components: {
    Header,
    Products,
    Footer
  },
  data() {
    return {
      products
    }
  }
}
</script>

<style scoped>
</style>
