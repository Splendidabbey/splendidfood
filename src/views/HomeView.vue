<template>

  <div class="splash-container">
    <div class="splash">
      <h1>Splendid Food</h1>
    </div>
  </div>

  <main class="wrapper">

    <h2>Recommended</h2>

    <div class="recommended">

      <ProductCardVue v-for="(product, index) in inventory.slice(0,3)" :productIcon="product.icon" :key="product.id" :index="index" :product="product" :addToCart="addToCart"/>

    </div>

  </main>
</template>

<script>
import ProductCardVue from '@/components/ProductCard.vue'

export default {
  name: 'HomeView',
  props: ['inventory', 'addToCart'],
  components: {
    ProductCardVue
  }
}
</script>
