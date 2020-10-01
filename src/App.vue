<template>
  <v-app>
    <v-container>
      <v-row>
        <v-col cols="12" sm="10" md="8"  class="mx-auto">
          <!-- <v-overlay :value="loading">
            <v-progress-circular indeterminate size="64"></v-progress-circular>
          </v-overlay> -->
          </v-col>
        </v-row>
      </v-container>
    <router-view/>
  </v-app>
</template>

<script>
export default {
  name: 'App',

  components: {
  },

  data: () => ({
    //
  }),
};
</script>
