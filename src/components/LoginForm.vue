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
      <v-list-item-title class="text-center">Iniciar Sesión</v-list-item-title>
      <!--Inputs -->
      <v-list dense>
        <v-list-item>
          <v-list-item-content>
            <v-card-text>
              <v-form>
                <v-text-field label='Correo Electrónico' 
                prepend-icon='mdi-account-circle-outline'
                color="#0F7740"
                />
                <v-text-field label='Contraseña' :type="showPassword ? 'text' : 'password'"
                  prepend-icon='mdi-lock-outline'
                  :append-icon="showPassword ? 'mdi-eye-outline' : 'mdi-eye-off-outline'"
                  @click:append="showPassword = !showPassword" 
                  color="#0F7740"
                  />
                <!-- Texto olvidar contraseña -->
                <v-text ><a href="" class="ref_color_text">Olvidaste tu contraseña</a></v-text>  
              </v-form>
            </v-card-text>
            <!-- Boton iniciar sesion -->
            <div  class="text-center">
              <v-btn
                dark
                color="#0F7740"    
                @click="login"
                >
                Iniciar Sesión
              </v-btn>
            </div>
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <v-divider></v-divider>
      <!--Icont Account --> 
      <div class="icon">
        <v-icon size="99px" >
          mdi-account-circle-outline
        </v-icon>
      </div>

        
     
    
    </v-navigation-drawer>
  </v-sheet>
</template>

<script>
  export default {
    data () {
      return {
        drawer: null,
      }
    },
  }
</script>

<style>
/* Tamaño imagen avatar */
.size_avatar{
  height: 99px !important;
  min-width: 99px !important;
}
/* Letras */
.ref_color_text {
  text-decoration: none;
  color: grey !important;
  margin-left: 1.5em;
}
.icon{
  text-align: center;
   
}
</style>