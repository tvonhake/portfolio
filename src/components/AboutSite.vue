<template>
  <v-container
    fluid
    fill-height
    grid-list-lg
    class="site-details"
    style="max-height: 100vh; max-width: 100vw"
  >
    <v-layout justify-center align-center column pa-5>
      <v-layout row mb-n16>
        <v-flex xs12 mb-n16 class="text-xs-center white--text display-1"
          >About This Site</v-flex
        >
      </v-layout>
      <v-flex mt-n16>
        <div class="headline white--text mt-3">Library:</div>
        <p class="subheading white--text mt-3">Vue</p>
        <div class="headline white--text mt-3">Styling:</div>
        <p class="subheading white--text mt-3">Vuetify and Material Design</p>
        <div class="headline white--text mt-3">Author:</div>
        <p class="subheading white--text mt-3">Trevor von Hake</p>
        <div class="headline white--text mt-3">Git Repository:</div>
        <p class="subheading white--text mt-3">Trevor von Hake</p>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: 'AboutSite',
};
</script>

<style scoped>
.site-details {
  background-color: rgb(54, 54, 54);
  width: 100% !important;
  height: 100%;
}
</style>
