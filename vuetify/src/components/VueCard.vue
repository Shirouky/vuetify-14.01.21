<template>
  <v-card class="mx-auto" max-width="344">
    <v-img
      :src="item.urlToImage"
      height="200px"
    ></v-img>

    <v-card-title> {{item.title}} </v-card-title>

    <v-card-subtitle> {{item.description}} </v-card-subtitle>

    <v-card-actions>
      <v-btn color="orange lighten-2" text> Explore </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
  export default {
    props: ["item"]
  }
</script>