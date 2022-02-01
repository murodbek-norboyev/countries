<template>
  <v-app-bar
    app>
    <h2 @click="goBack()">Where in the world?</h2>

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
    goBack () {
      this.$router.push({ path: '/' })
    },
    darkMode () {
      this.$vuetify.theme.dark = !this.$vuetify.theme.dark
    }
  }
}
</script>

<style scoped>

</style>
