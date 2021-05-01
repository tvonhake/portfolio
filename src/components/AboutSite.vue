<template>
  <v-container
    fluid
    fill-height
    grid-list-lg
    class="site-details"
    style="max-height: 100vh; max-width: 100vw"
  >
    <v-layout justify-center align-center column pa-5>
      <v-layout row>
        <v-flex xs12 class="text-xs-center white--text display-1 my-5"
          >About This site</v-flex
        >
      </v-layout>
      <v-flex>
        <div class="headline white--text mt-3">Built Using</div>
        <p class="subheading white--text mt-3">
          Vue Vuetify Material UI Netlify
        </p>
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
