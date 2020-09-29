<template>
  <v-sheet
    class="mx-auto"
    max-width="290"
  >
    <v-slide-group
      active-class="success"
      show-arrows
    >
      <v-slide-item
        v-for="n in 15"
        :key="n"
        v-slot:default="{ active, toggle }"
      >
        <v-btn
          class="mx-2"
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
</template>
