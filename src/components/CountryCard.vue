<template>
  <v-col cols="12" sm="4" lg="3">
    <v-card
      @click="goCountryDetailPage">
      <v-img height="200" :src="countryData.flag"></v-img>
      <v-card-title>{{ countryData.name }}</v-card-title>
      <v-card-text>
        <p><strong>Population: </strong> {{ countryData.population }}</p>
        <p><strong>Region: </strong> {{ countryData.region }}</p>
        <p class="mb-0"><strong>Capital: </strong> {{ countryData.capital }}</p>
      </v-card-text>
    </v-card>
  </v-col>
</template>

<script>
export default {
  name: 'CountryCard',
  props: {
    countryData: Object
  },
  methods: {
    goCountryDetailPage () {
      this.$router.push({ path: `${this.countryData.name}` })
    }
  }
}
</script>

<style scoped>

</style>
