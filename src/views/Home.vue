<template>
  <div class="home">
    <product-card/>
   
    <login-form/>
  </div>
</template>

<script>
import ProductCard from '../components/ProductCard'
import LoginForm from '../components/LoginForm'

export default {
  name: 'Home',
  components: {
    ProductCard,
    LoginForm
  }
}
</script>
