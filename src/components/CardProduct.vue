<template>
  <div>      
    <v-card
      :loading="loading"
      class="mx-auto my-12"
      max-width="280"
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

      <v-card-title class="color_text size_title font-weight-medium">Za'atar Verde</v-card-title>
      <div class="d-flex">
      <v-card-text class="pr-0" >
        <h2 class="color_text size_subtitle font-weight-light">Unidades:</h2>
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

      <v-card-title class="color_text size_subtitle font-weight-light">Elige la Presentación:</v-card-title>

      <v-card-text >
        <v-chip-group
          v-model="selection"
          active-class="red white--text"
          
          class="section__btn"
        >
          <v-chip class="border_btn color_btn color_btn_text ">100 g</v-chip>

          <v-chip class="border_btn color_btn color_btn_text">500 g</v-chip>

          <v-chip class="border_btn color_btn color_btn_text">1 kg</v-chip>
        </v-chip-group>
      </v-card-text>

      <v-divider class="mx-4"></v-divider>

      <v-card-actions class="pa-2">
        <div class="text-center">
          <h2 class="color_text size_price font-weight-medium">$3500</h2>
          <h4 class="color_text size_final_price font-weight-light">Precio final por 3 Unidades de 1Kg</h4>
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
/* Título card */
.size_title {
  font-size: 20px !important;
}
/* Subtitulos de la card */
.size_subtitle {
  font-size: 18px !important;
} 
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
/* Colores del texto de la card */
.color_text{
  color:#737373 !important;
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
} 
 /* Tamaño letra precio */
.size_price {
  font-size: 22px !important;
}
/* Tamaño descripción precio final */
.size_final_price {
  font-size: 13px !important;
}
</style>