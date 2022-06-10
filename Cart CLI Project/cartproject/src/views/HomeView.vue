<template>
  <div class="splash-container">
    <div class="splash">
      <h1>Splendid Food</h1>
    </div>
  </div>

  <main class="wrapper">

    <h2>Recommended</h2>

    <div class="recommended">

      <Card-Widget v-for="(product, index) in inventory.slice(0,3)"
        :key="product.id"
        class="card"
        :index="index"
        :product="product"
        :addToCart="addToCart"
      />

    </div>

  </main>
</template>

<script>
import CardWidget from '@/components/CardWidget.vue'

export default {
  name: 'HomeView',
  props: ['inventory', 'addToCart'],
  components: {
    CardWidget
  }
}
</script>
