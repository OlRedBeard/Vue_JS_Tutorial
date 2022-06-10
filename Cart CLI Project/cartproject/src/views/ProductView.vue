<template>
    <main class="wrapper">
        <h1>Products</h1>

        <div class="card-container">
            <Card-Widget v-for="(product, index) in inventory"
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
  props: ['inventory', 'addToCart'],
  components: {
    CardWidget
  }
}
</script>
