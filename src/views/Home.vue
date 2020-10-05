<template>
  <div class="home">   
    <product-tag/>
    <v-container>
      <v-row>
        <v-col cols="12" class="mx-auto">
          <v-sheet
            class="mx-auto"
            
          >
          <v-slide-group
              active-class="success"
          > 
              <product-card/>
              <card-product/>
          </v-slide-group>
          </v-sheet> 
          <v-btn
            dark
            color="#1AA3C1"
            class="pa-3 ml-2 font-weight-light"
            style="border-radius: 10px;"
          >
            Ver Todos los Productos Arabes 
            
          </v-btn>    
        </v-col>
      </v-row>
    </v-container>
    <login-form/>
    <card-detail/>
  </div>
</template>

<script>
import ProductTag from '../components/ProductTag'
import ProductCard from '../components/ProductCard'
import CardProduct from '../components/CardProduct'
import LoginForm from '../components/LoginForm'
import CardDetail from '../components/CardDetail'

export default {
  name: 'Home',
  components: {
    ProductTag,
    ProductCard,
    CardProduct,
    LoginForm,
    CardDetail
  }
}
</script>
