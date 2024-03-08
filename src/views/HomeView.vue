<template>
  <section class="container">
    <range-selector :products="filteredProducts" v-model="max" />
    <product-list :products="filteredProducts"></product-list>
  </section>
</template>

<script>
import ProductList from '@/components/ProductList'
import RangeSelector from '@/components/RangeSelector.vue'

export default {
  name: 'HomeView',
  data: function () {
    return {
      max: 50,
      cart: []
    }
  },
  props: ['products'],
  components: {
    ProductList,
    RangeSelector
  },
  computed: {
    filteredProducts() {
      return this.products.filter(item => item.price < Number(this.max))
    }
  }
}
</script>
