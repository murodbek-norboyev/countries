<template>
  <v-container>
    <v-row class="mt-4">
      <v-col cols="2">
        <v-btn
          class="text-capitalize"
          @click="goBack">
          <font-awesome-icon class="mr-2" icon="chevron-left"/>
          go back
        </v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import { mapState } from 'vuex'

export default {
  name: 'CountryDetail',
  props: {
    countryData: Object
  },
  computed: {
    ...mapState(['countries'])
  },
  methods: {
    goBack () {
      this.$router.push({ path: '/' })
    }
  }
}
</script>

<style scoped>

</style>
