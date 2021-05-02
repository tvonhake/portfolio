<template>
  <v-container
    fluid
    fill-height
    class="projects"
    grid-list-lg
    style="max-height: 100vh; max-width: 100vw"
  >
    <v-slide-group
      v-model="model"
      class="pa-0 ma-0"
      show-arrows
      center-active
      dark
    >
      <v-slide-item v-for="n in 1" :key="n" v-slot="{ toggle }">
        <v-hover v-slot:default="{ hover }">
          <v-flex xs12 sm12 md4 mx-10>
            <v-card
              :color="transparent"
              class="ma-4"
              height="75vh"
              width="375px"
              @click="toggle"
            >
              <v-img src="https://i.imgur.com/6FL7jsq.png" height="500px">
                <v-expand-transition>
                  <div
                    v-if="hover"
                    class="d-flex transition-fast-in-fast-out grey darken-2 v-card--reveal display-3 white--text"
                    style="height: 100%"
                  >
                    A digital replacement for physical vaccination proof
                  </div>
                </v-expand-transition>
              </v-img>

              <v-card-title primary-title>
                <v-row dense>
                  <h3 class="headline mb-0 mr-5">Vaccine Passport</h3>
                  <v-spacer />
                  <v-btn
                    medium
                    color="transparent"
                    depressed
                    dark
                    mr-n8
                    href="https://vaccine-passport.herokuapp.com/"
                    target="_blank"
                  >
                    <v-icon medium color="white">{{ Web }}</v-icon>
                  </v-btn>
                  <v-btn
                    medium
                    color="transparent"
                    depressed
                    dark
                    href="https://github.com/Derek229/vaccine-passport"
                    target="_blank"
                  >
                    <v-icon medium color="white">{{ GitHub }}</v-icon>
                  </v-btn>
                </v-row>
              </v-card-title>
            </v-card>
          </v-flex>
        </v-hover>
      </v-slide-item>

      <v-slide-item v-for="n in 1" :key="n" v-slot="{ toggle }">
        <v-hover v-slot:default="{ hover }">
          <v-flex xs12 sm12 md4 mx-10>
            <v-card
              :color="transparent"
              class="ma-4"
              height="75vh"
              width="375px"
              @click="toggle"
            >
              <v-img src="https://i.imgur.com/7nMgRVt.png" height="500px">
                <v-expand-transition>
                  <div
                    v-if="hover"
                    class="d-flex transition-fast-in-fast-out grey darken-2 v-card--reveal display-3 white--text"
                    style="height: 100%"
                  >
                    React Native Mobile App for Vaccine Passport
                  </div>
                </v-expand-transition>
              </v-img>
              <v-card-title primary-title>
                <v-row dense>
                  <h3 class="headline mb-0">Vaccine Passport Mobile</h3>
                  <v-spacer />
                  <v-btn
                    medium
                    color="transparent"
                    depressed
                    dark
                    href="https://github.com/tvonhake/VaccinePassport-ReactNativeWebView"
                    target="_blank"
                  >
                    <v-icon medium color="white">{{ GitHub }}</v-icon>
                  </v-btn>
                </v-row>
              </v-card-title>
            </v-card>
          </v-flex>
        </v-hover>
      </v-slide-item>

      <v-slide-item v-for="n in 1" :key="n" v-slot="{ toggle }">
        <v-hover v-slot:default="{ hover }">
          <v-flex xs12 sm12 md4 mx-10>
            <v-card
              :color="transparent"
              class="ma-4"
              height="75vh"
              width="375px"
              @click="toggle"
            >
              <v-img src="https://i.imgur.com/3ThKo6y.png" height="500px">
                <v-expand-transition>
                  <div
                    v-if="hover"
                    class="d-flex transition-fast-in-fast-out grey darken-2 v-card--reveal display-3 white--text"
                    style="height: 100%"
                  >
                    community-driven social media for music sharing
                  </div>
                </v-expand-transition>
              </v-img>
              <v-card-title primary-title>
                <v-row dense>
                  <h3 class="headline mb-0 mr-16">Musn</h3>
                  <v-spacer />
                  <v-btn
                    medium
                    color="transparent"
                    depressed
                    dark
                    ml-16
                    mr-0
                    href="https://github.com/Derek229/Musn"
                    target="_blank"
                  >
                    <v-icon medium color="white">{{ GitHub }}</v-icon>
                  </v-btn>
                </v-row>
              </v-card-title>
            </v-card>
          </v-flex>
        </v-hover>
      </v-slide-item>
    </v-slide-group>
  </v-container>
</template>

<script>
import { mdiGithub, mdiWeb } from '@mdi/js';
export default {
  name: 'Projects',
  data: () => ({
    model: null,
    Web: mdiWeb,
    GitHub: mdiGithub,
  }),
};
</script>

<style scoped>
.projects {
  background: url('http://source.unsplash.com/AoNvwL-Dmtw');
  background-size: cover;
  width: 100% !important;
  height: 100%;
}
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: 0.9;
  position: absolute;
  width: 100%;
}
</style>
