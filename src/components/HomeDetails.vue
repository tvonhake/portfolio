<template>
  <v-container
    fluid
    fill-height
    grid-list-lg
    class="home-details"
    style="max-height: 100vh; max-width: 100vw"
  >
    <v-layout justify-center align-center column pa-5>
      <v-layout row>
        <v-flex xs12 class="text-xs-center white--text display-1 my-5"
          >About Me</v-flex
        >
      </v-layout>
      <v-flex>
        <div class="headline white--text mt-3">Skills</div>
        <p class="subheading white--text mt-3">
          Javascript React.js Vue Ruby Ruby on Rails HTML5 CSS3 Bootstrap
          Semantic Material UI Postgresql Postman API
        </p>
      </v-flex>
      <v-flex>
        <div class="headline white--text mt-3">Education</div>
        <p class="subheading white--text mt-3">
          DevPoint Labs Full Stack Web Development - University of Utah BS
          Psychology
        </p>
      </v-flex>
      <v-flex>
        <div class="headline white--text mt-3">Learn More</div>
        <p class="subheading white--text mt-3">LinkedIn Github</p>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: 'HomeDetails',
};
</script>

<style scoped>
.home-details {
  background-color: rgb(54, 54, 54);
  width: 100% !important;
  height: 100%;
}
</style>
