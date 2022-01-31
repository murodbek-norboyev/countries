<template>
  <v-container v-if="load === true">
    <filter-bar/>
    <v-row>
      <v-col></v-col>
    </v-row>
  </v-container>
  <loading v-else></loading>
</template>
<script>
import FilterBar from '../components/FilterBar'
import Loading from '../components/loading'

export default {
  components: {
    Loading,
    FilterBar
  },
  data: () => ({
    load: false
  })
}
</script>
