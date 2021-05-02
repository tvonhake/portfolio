<template>
  <v-container
    fluid
    fill-height
    grid-list-lg
    class="site-details"
    style="max-height: 100vh; max-width: 100vw"
  >
    <!-- <v-layout justify-center align-center column pa-5>
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
        <div class="headline white--text mt-3">Git Repository:</div>
        <p class="subheading white--text mt-3">Trevor von Hake</p>
      </v-flex>
    </v-layout> -->
    <v-slide-group dark v-model="model" class="pa-4" center-active show-arrows>
      <v-slide-item v-for="n in 1" :key="n" v-slot:default="{ active }">
        <v-card
          :color="active ? 'transparent' : 'transparent'"
          class="ma-4"
          height="600px"
          width="85vw"
          flat
          dark
        >
          <v-img
            contain
            max-height="600px"
            src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/1184px-Vue.js_Logo_2.svg.png"
          >
            <v-row class="fill-height" align="center" justify="center">
              <h3 class="headline">Created with Vue</h3>
            </v-row>
          </v-img>
        </v-card>
      </v-slide-item>
      <v-slide-item v-for="n in 1" :key="n" v-slot:default="{ active }">
        <v-card
          :color="active ? 'transparent' : 'transparent'"
          class="ma-4"
          height="600px"
          width="85vw"
          flat
          dark
        >
          <v-img
            contain
            max-height="600px"
            src="https://i.imgur.com/6yw7mnT.png"
          >
            <v-row class="fill-height" align="center" justify="center">
              <h3 class="headline">Styled with Vuetify</h3>
            </v-row>
          </v-img>
        </v-card>
      </v-slide-item>
      <v-slide-item v-for="n in 1" :key="n" v-slot:default="{ active }">
        <v-card
          :color="active ? 'transparent' : 'transparent'"
          class="ma-4"
          height="600px"
          width="85vw"
          flat
          dark
        >
          <v-img
            contain
            max-height="600px"
            src="https://i.imgur.com/b4Ejv2Y.png"
          >
            <v-row class="fill-height" align="center" justify="center">
              <a
                class="git-link"
                href="https://github.com/tvonhake/portfolio"
                target="_blank"
                ><h3 class="headline">View Repository</h3></a
              >
            </v-row>
          </v-img>
        </v-card>
      </v-slide-item>
    </v-slide-group>
  </v-container>
</template>

<script>
export default {
  name: 'AboutSite',
  data: () => ({
    model: undefined,
  }),
};
</script>

<style scoped>
.site-details {
  background-color: rgb(54, 54, 54);
  width: 100% !important;
  height: 100%;
}
h3 {
  text-shadow: 1px 1px #353535;
}
.git-link {
  color: white;
  text-decoration: none;
}
</style>
