<template>
  <v-container v-if="filteredCountries.length > 0">
    <filter-bar/>
    <v-row>
      <country-card
        v-for="(country, i) in filteredCountries"
        :key="i"
        :countryData="country"
      />
    </v-row>
  </v-container>
  <loading v-else></loading>
</template>
<script>
import FilterBar from '../components/FilterBar'
import Loading from '../components/loading'
import CountryCard from '../components/CountryCard'
import { mapState, mapActions } from 'vuex'

export default {
  components: {
    CountryCard,
    Loading,
    FilterBar
  },
  data: () => ({ }),
  computed: {
    ...mapState(['countries', 'region']),
    filteredCountries () {
      if (this.region === 'All' || this.region === null) {
        return this.countries
      } else {
        return this.countries.filter(
          (country) => country.region === this.region
        )
      }
    }
  },
  methods: {
    ...mapActions(['getAllCountries', 'filterRegion'])
  },
  watch: {
    region (val) {
      if (val === null) {
        this.filterRegion(null)
      }
    }
  },
  mounted () {
    this.getAllCountries()
  }
}
</script>
