<template>
  <div>
    <v-btn block
      max-height="374"> 
      Block Button
      <v-img
        height="150"
      src="https://picsum.photos/1920/1080?random"
      ></v-img>   
    </v-btn>
    <v-card
      :loading="loading"
      class="mx-auto my-12"
      max-width="374"
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

      <v-card-title class="color_text font-weight-medium">Za'atar Rojo</v-card-title>
      <div class="d-flex">
      <v-card-text class="pr-0" >
        <h2 class="color_text font-weight-light">Unidades:</h2>
      </v-card-text>
      <v-sheet
        class="mx-auto pt-2"
        max-width="210"
      >
        <v-slide-group
          active-class="#EB4040"
          show-arrows
        >
          <v-slide-item
            v-for="n in 10"
            :key="n"
            v-slot:default="{ active, toggle }"
          >
            <v-btn
              class="mx-1 pa-1 color_btn color_btn_text border_btn"
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

      <v-card-title class="color_text font-weight-light">Elige la Presentación:</v-card-title>

      <v-card-text >
        <v-chip-group
          v-model="selection"
          active-class="red accent-4 white--text"
          
          class="section__btn"
        >
          <v-chip class=" border_btn color_btn color_btn_text ">100 mg</v-chip>

          <v-chip class=" border_btn color_btn color_btn_text">500 mg</v-chip>

          <v-chip class=" border_btn color_btn color_btn_text">1 kg</v-chip>
        </v-chip-group>
      </v-card-text>

      <v-divider class="mx-4"></v-divider>

      <v-card-actions class="pa-2">
        <div>
          <h2 class="color_text font-weight-medium">$3500</h2>
          <h4 class="color_text font-weight-light">Precio final por 1 Unidad de 1Kg</h4>
        </div>
        <v-btn
          dark
          class="pa-5 font-weight-light btn__add"
          @click="sell"
        >
          Añadir al Carrito
        </v-btn>
      </v-card-actions>
    </v-card>
  </div>
</template>

<script>
  export default {
    data: () => ({
      loading: false,
      selection: 1,
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
.border_btn{
  border-radius: 10px !important;
  padding: 1.5em 1.7em 1.5em 1.7em !important;
}
.color_text{
  color:#737373 !important;
}
.color_btn_text{
  color: #ffff !important;
}
.color_btn{
  background-color:#C4C4C4 !important;
}
/* Seccion botones de medicion */
/* .section__btn {
  display: flex;
  justify-content: space-between !important;
} */

/* Boton añadir carrito */
.btn__add {
  background-color: #67CC38 !important;
}  

</style>