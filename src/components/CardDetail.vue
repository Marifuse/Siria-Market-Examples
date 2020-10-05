<template>
  <div>      
    <v-card
      :loading="loading"
      class="mx-auto my-12 mr-4"
      max-width="310"
    >
      <template slot="progress">
        <v-progress-linear
          color="deep-purple"
          height="10"
          indeterminate
        ></v-progress-linear>
      </template>

      <v-img
        height="250"
        src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
      ></v-img>

      <v-card max-width="270" class="mx-auto" style="border-radius: 2em;">
        <v-btn
          dark
          class="pl-4 pr-4 ml-3 mt-3 font-weight-light"
          style="border-radius: 1em;"
          color="#2E6A3B"
        >
          <span>Arabe</span> 
        </v-btn>
        <v-card-title class="font-weight-medium pb-0" style="font-size: 20px; color:#737373;">Za'atar Rojo</v-card-title>
        <p class="pa-5 mb-0 font-weight-medium" style="font-size: 15px; color:#585858;">Small plates, salads & sandwiches - an intimate setting with 12 indoor seats plus patio seating.</p>
        <div class="d-flex">
        <v-card-text class="pr-0" >
          <h2 class="font-weight-light" style="font-size: 18px; color:#737373;">Unidades:</h2>
        </v-card-text>
        <v-sheet
          class="mx-auto pt-2 pr-2"
          max-width="150"
        >
          <v-slide-group
            active-class="#EB4040"
            mandatory
          >
            <v-slide-item
              v-for="n in 10"
              :key="n"
              v-slot:default="{ active, toggle }"
            >
              <v-btn
                class="mx-1 pa-1 color_btn color_btn_text border_btn size_btn"
                :input-value="active"
                active-class="red white--text"
                depressed
                @click="toggle"
              >
                {{ n }}
              </v-btn>
            </v-slide-item>
          </v-slide-group>
        </v-sheet>
      </div>

        <v-card-title class="font-weight-light" style="font-size: 18px; color:#737373;">Elige la Presentación:</v-card-title>

        <v-card-text >
          <v-chip-group
            v-model="selection"
            active-class="red white--text"
            
            class="section__btn"
          >
            <v-chip class="border_btn color_btn color_btn_text">100 g</v-chip>

            <v-chip class="border_btn color_btn color_btn_text">500 g</v-chip>

            <v-chip class="border_btn color_btn color_btn_text">1 kg</v-chip>
          </v-chip-group>
        </v-card-text>

        <v-divider class="mx-4"></v-divider>

      </v-card>
      <v-card-actions class="pa-2">
        <div class="text-center">
          <h2 class="font-weight-medium" style="font-size: 22px; color:#737373;">$3500</h2>
          <h4 class="font-weight-light" style="font-size: 13px; color:#737373;">Precio final por 3 Unidades de 1Kg</h4>
        </div>
        <v-btn
          dark
          class="pa-3 ml-2 font-weight-light btn__add"
          @click="sell"
        >
          Añadir 
          <v-icon size="20px">
            mdi-cart-variant
          </v-icon>
        </v-btn>
      </v-card-actions>
    </v-card>
  </div>
</template>

<script>
  export default {
    data: () => ({
      loading: false,
      selection: 0,
    }),

    methods: {
      reserve () {
        this.loading = true
        setTimeout(() => (this.loading = false), 2000)
      },
    },
  }
</script>

<style>
/* Botones de unidades */
.size_btn {
  height: 40px !important;
  min-width: 44px !important;
}
/* Botones presentaciones */
.border_btn{
  border-radius: 10px !important;
  padding: 1em 1.5em 1em 1.5em !important;
  font-size: 18px !important;
}
/* Color texto de botones */
.color_btn_text{
  color: #ffff !important;
}
/* Colores de los botones */
.color_btn{
  background-color:#C4C4C4 !important;
}
/* Boton añadir carrito */
.btn__add {
  background-color: #67CC38 !important;
  border-radius: 10px !important;
}
</style>