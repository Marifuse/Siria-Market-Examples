<template>
  <div class="home">
    <product-tag/>
    <product-card/>
    <login-form/>
  </div>
</template>

<script>
import ProductTag from '../components/ProductTag'
import ProductCard from '../components/ProductCard'
import LoginForm from '../components/LoginForm'

export default {
  name: 'Home',
  components: {
    ProductTag,
    ProductCard,
    LoginForm
  }
}
</script>
