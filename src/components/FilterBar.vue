<template>
  <v-row justify="space-between">
    <v-col
      cols="4">
      <v-text-field
        label="Search"
        v-model="search"
        solo
        clearable>

      </v-text-field>
    </v-col>
    <v-col
      cols="3">
      <v-select
        label="Select region"
        :items="regions"
        solo>
      </v-select>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'FilterBar',
  data: () => ({
    search: null,
    regions: ['All', 'Asia', 'Africa', 'Europe', 'Americas', 'Oceania']
  })
}
</script>

<style scoped>

</style>
