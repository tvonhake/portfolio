<template>
  <v-container
    fill-height
    class="projects"
    grid-list-lg
    style="max-height: 100vh; max-width: 100vw"
  >
    <v-layout column pa-5>
      <v-layout row>
        <v-flex xs12 class="text-xs-center white--text display-1 font-weight-black my-5"
          >Projects</v-flex
        >
      </v-layout>
      <v-layout row wrap>
        <v-flex xs12 sm12 md4>
          <v-card>
            <v-img src="https://i.imgur.com/6FL7jsq.png" height="500px">
              <v-container fill-height fluid>
                <v-layout fill-height>
                  <v-flex xs12 align-end flexbox> </v-flex>
                </v-layout>
              </v-container>
            </v-img>

            <v-card-title primary-title>
              <div>
                <h3 class="headline mb-0">Vaccine Passport</h3>
                <div>Description here.</div>
              </div>
            </v-card-title>
          </v-card>
        </v-flex>

        <v-flex xs12 sm12 md4>
          <v-card>
            <v-img src="https://i.imgur.com/3ThKo6y.png" height="500px">
              <v-container fill-height fluid>
                <v-layout fill-height>
                  <v-flex xs12 align-end flexbox> </v-flex>
                </v-layout>
              </v-container>
            </v-img>
            <v-card-title primary-title>
              <div>
                <h3 class="headline mb-0">Musn</h3>
                <div>Description here</div>
              </div>
            </v-card-title>
          </v-card>
        </v-flex>

        <v-flex xs12 sm12 md4>
          <v-card>
            <v-img src="https://i.imgur.com/7nMgRVt.png" height="500px">
              <v-container fill-height fluid>
                <v-layout fill-height>
                  <v-flex xs12 align-end flexbox> </v-flex>
                </v-layout>
              </v-container>
            </v-img>
            <v-card-title primary-title>
              <div>
                <h3 class="headline mb-0">Vaccine Passport App</h3>
                <div>Description here</div>
              </div>
            </v-card-title>
          </v-card>
        </v-flex>
      </v-layout>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: 'Projects',
};
</script>

<style scoped>
.projects {
  background: url('http://source.unsplash.com/AoNvwL-Dmtw');
  background-size: cover;
  width: 100% !important;
  height: 100%;
  margin: 0 !important;
  padding: 0 !important;
}
</style>
