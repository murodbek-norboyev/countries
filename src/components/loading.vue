<template>
  <v-container>
    <v-row>
      <v-col
        cols="3"
      >
        <v-skeleton-loader
          v-bind="attrs"
          type="image, article"
        ></v-skeleton-loader>
      </v-col>
       <v-col
        cols="3"
      >
        <v-skeleton-loader
          v-bind="attrs"
          type="image, article"
        ></v-skeleton-loader>
      </v-col>
       <v-col
        cols="3"
      >
        <v-skeleton-loader
          v-bind="attrs"
          type="image, article"
        ></v-skeleton-loader>
      </v-col>

       <v-col
        cols="3"
      >
        <v-skeleton-loader
          v-bind="attrs"
          type="image, article"
        ></v-skeleton-loader>
      </v-col>
       <v-col
        cols="3"
      >
        <v-skeleton-loader
          v-bind="attrs"
          type="image, article"
        ></v-skeleton-loader>
      </v-col>
       <v-col
        cols="3"
      >
        <v-skeleton-loader
          v-bind="attrs"
          type="image, article"
        ></v-skeleton-loader>
      </v-col>
       <v-col
        cols="3"
      >
        <v-skeleton-loader
          v-bind="attrs"
          type="image, article"
        ></v-skeleton-loader>
      </v-col>
       <v-col
        cols="3"
      >
        <v-skeleton-loader
          v-bind="attrs"
          type="image, article"
        ></v-skeleton-loader>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'loading',
  data: () => ({
    attrs: {
      boilerplate: false,
      elevation: 2
    }
  })
}
</script>

<style scoped>

</style>
