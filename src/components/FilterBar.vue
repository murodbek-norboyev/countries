<template>
  <v-col>
    <v-text-field
      label="Search"
      v-model="search"
      solo
      clearable
    ></v-text-field>
  </v-col>
  <v-col></v-col>
</template>

<script>
export default {
  name: 'FilterBar'
}
</script>

<style scoped>

</style>
