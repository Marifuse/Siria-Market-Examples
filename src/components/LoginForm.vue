<template>
  <v-sheet
    height="400"
    class="overflow-hidden"
    style="position: relative;"
  >
    <v-container class="fill-height">
      <v-row
        align="center"
        justify="center"
      >
        <v-btn
          color="pink"
          dark
          @click.stop="drawer = !drawer"
        >
          Toggle
        </v-btn>
      </v-row>
    </v-container>

    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
    >
    <!--Form -->
      <v-list-item>
        <v-list-item-avatar class="mx-auto size_avatar">
          <v-img src="../assets/logo_siria.png"></v-img>
        </v-list-item-avatar>
        
      </v-list-item>
      <v-list-item-title class="text-center font-weight-black size_title">Iniciar Sesión</v-list-item-title>
      <!--Inputs -->
      <v-list dense>
        <v-list-item>
          <v-list-item-content>
            <v-card-text>
              <v-form>
                <v-text-field label='Correo Electrónico'
                  v-model="email" 
                  prepend-icon='mdi-account-circle-outline'
                  color="#0F7740"
                />
                <v-text-field label='Contraseña'
                  prepend-icon='mdi-lock-outline'
                  append-icon='mdi-eye-off-outline'
                  color="#0F7740"
                  />  
              </v-form>
            </v-card-text>
            <div  class="text-center">
              <!-- Texto olvidar contraseña -->
              <v-text><a href="" class="ref_color_text">Olvidaste tu contraseña</a></v-text>
              <!-- Boton iniciar sesion -->
              <v-btn
                class="mt-5 mb-5"
                dark
                color="#0F7740"        
                >
                Iniciar Sesión
              </v-btn>
            </div>
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <v-divider></v-divider>
      <!--Icont Account --> 
      <div class="icon mt-5">
        <v-icon size="99px">
          mdi-account-circle-outline
        </v-icon>
        <h4 class="subtitle_color_text">¿No tienes Cuenta?</h4>
        <v-text><a href="" class="ref_color_text_2 mb-5">Regístrate</a></v-text> 
        <br>
        <v-btn
          class="mt-5 mb-5"
          color="#535353"
          text
          @click="drawer = false"
         
        >
          Cerrar X
        </v-btn>
      </div>
    </v-navigation-drawer>
  </v-sheet>
</template>

<script>
  export default {
    data () {
      return {
        drawer: null,
        email : "",
      }
    },
    methods: {
    }
  }   
</script>

<style>
/* Tamaño imagen avatar */
.size_avatar{
  height: 99px !important;
  min-width: 99px !important;
}
/* Texto */
/* Titulo Iniciar Sesion */
.size_title {
  font-size: 18px !important;
  color: #535353 !important;
}
/* Primer href */
.ref_color_text {
  text-decoration: none;
  color: grey !important;
  margin-bottom: 1em !important;
}
/* Pregunta y 2do href */
.subtitle_color_text, .ref_color_text_2 {
  color: #EB4040 !important;
  text-decoration: none;
  font-size: 18px;
}
.ref_color_text_2 {
  font-weight: 700;
}
/* Icono */
.icon{
  text-align: center;
}
</style>