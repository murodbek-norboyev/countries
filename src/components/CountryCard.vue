<template>
  <v-col cols="3">
    <v-card
      @click="goCountryDetailPage">
      <v-img height="150" :src="countryData.flag"></v-img>
      <v-card-title>{{ countryData.name }}</v-card-title>
      <v-card-text>
        <p><strong>Population: </strong> {{ countryData.population }}</p>
        <p><strong>Region: </strong> {{ countryData.region }}</p>
        <p><strong>Capital: </strong> {{ countryData.capital }}</p>
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
  filters: {
    // capitalize more than one space seperated words
    showDecimalPoint (val) {
      return val.toString().replace(/\B(?=(\d{3})+(?!\d))/g, '.')
    }
  },
  methods: {
    goCountryDetailPage () {
      this.$router.push({ path: `/${this.countryData.name}` })
    }
  }
}
</script>

<style scoped>

</style>
