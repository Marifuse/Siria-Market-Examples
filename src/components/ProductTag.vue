<template>
  <div>
     <v-app-bar
      absolute
      color="#fcb69f"
      dark
      shrink-on-scroll
      src="https://picsum.photos/1920/1080?random"
      scroll-target="#scrolling-techniques-2"
      style="height: 70px;"
    >
      <template v-slot:img="{ props }">
        <v-img 
          v-bind="props"
          gradient="to top right, rgba(19,84,122,.5), rgba(128,208,199,.8)"
        ></v-img>
      </template>

      <v-toolbar-title style="height: 110px;"><a href="" class="color_link">Productos Arabes</a></v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon style="height: 55px;">
        <v-icon >mdi-chevron-right</v-icon>
      </v-btn>
    </v-app-bar>
  </div>
</template>

<script>
  export default {
    name: 'ProductTag',

  }
</script>

<style>
/* Color del link del nav */
.color_link {
  text-decoration: none;
  color: #FFF !important;
}
</style>
