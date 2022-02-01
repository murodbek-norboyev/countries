<template>
  <v-container>
    <v-col cols="4">
      <v-btn
        @click="goBack">
        <font-awesome-icon icon="chevron-left" size="lg"/>
      </v-btn>
    </v-col>
  </v-container>
</template>

<script>
export default {
  name: 'CountryDetail',
  methods: {
    goBack () {
      this.$router.push({ path: '/' })
    }
  }
}
</script>

<style scoped>

</style>
