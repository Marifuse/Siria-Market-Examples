<template>
  <div class="home">
    <product-card/>
    <slide/>
  </div>
</template>

<script>
import ProductCard from '../components/ProductCard'
import Slide from '../components/Slide'

export default {
  name: 'Home',
  components: {
    ProductCard,
    Slide,
  }
}
</script>
