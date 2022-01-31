<template>
  <v-app-bar
    app>
    <div class="d-flex align-center"><h2>Where in the world?</h2></div>

    <v-spacer></v-spacer>

    <v-btn text @click="darkMode">
      <font-awesome-icon
        v-if="$vuetify.theme.dark"
        icon="sun"
        size="lg"
      />
      <font-awesome-icon v-else icon="moon" size="lg"/>
      <span class="ml-2">
        {{ $vuetify.theme.dark ? 'Light Mode' : 'Dark Mode' }}</span
      >
    </v-btn>

  </v-app-bar>
</template>

<script>
export default {
  name: 'NavBar',
  methods: {
    darkMode () {
      this.$vuetify.theme.dark = !this.$vuetify.theme.dark
    }
  }
}
</script>

<style scoped>

</style>
