<template>
  <v-row justify="space-between" class="mt-10 mb-5">
    <v-col
      cols="12"
      sm="6"
      md="4">
      <v-text-field
        label="Search"
        v-model="search"
        solo
        prepend-inner-icon="mdi-magnify"
        clearable>
      </v-text-field>
    </v-col>
    <v-col
      cols="12"
      sm="6"
      md="3">
      <v-select
        label="Select region"
        v-model="region"
        :items="regions"
        solo>
      </v-select>
    </v-col>
  </v-row>
</template>

<script>
import { mapActions } from 'vuex'

export default {
  name: 'FilterBar',
  data () {
    return {
      search: null,
      region: null,
      timeoutQuery: null,
      regions: ['All', 'Asia', 'Africa', 'Europe', 'Americas', 'Oceania']
    }
  },
  methods: {
    ...mapActions(['searchCountries', 'getAllCountries', 'filterRegion'])
  },
  watch: {
    search (query) {
      if (this.timeoutQuery) {
        clearTimeout(this.timeoutQuery)
      }
      if (query) {
        this.timeoutQuery = setTimeout(() => this.searchCountries(query), 300)
      } else {
        this.timeoutQuery = setTimeout(() => this.getAllCountries())
      }
    },
    region (val) {
      this.filterRegion(val)
    }
  }
}
</script>

<style scoped>

</style>
