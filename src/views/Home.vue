<template>
  <span>
    <v-app-bar app color="transparent" flat dense prominent dark>
      <v-app-bar-nav-icon
        @click="drawer = true"
        style="border-radius: 5px"
      ></v-app-bar-nav-icon>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" fixed temporary dark>
      <v-list nav dense>
        <v-list-item-group v-model="group">
          <v-list-item
            @click="
              $vuetify.goTo('#top');
              drawer = false;
            "
          >
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item>

          <v-list-item
            @click="
              $vuetify.goTo('#aboutme', { offset: -96 });
              drawer = false;
            "
          >
            <v-list-item-icon>
              <v-icon>{{ Account }}</v-icon>
            </v-list-item-icon>
            <v-list-item-title>About Me</v-list-item-title>
          </v-list-item>

          <v-list-item
            @click="
              $vuetify.goTo('#projects', { offset: -96 });
              drawer = false;
            "
          >
            <v-list-item-icon>
              <v-icon>{{ Folder }}</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Projects</v-list-item-title>
          </v-list-item>

          <v-list-item
            @click="
              $vuetify.goTo('#aboutsite', { offset: -96 });
              drawer = false;
            "
          >
            <v-list-item-icon>
              <v-icon>{{ Information }}</v-icon>
            </v-list-item-icon>
            <v-list-item-title>About This Site</v-list-item-title>
          </v-list-item>

          <a
            href="https://github.com/tvonhake"
            class="icon-link"
            target="_blank"
            ><v-list-item>
              <v-list-item-icon>
                <v-icon>{{ Github }}</v-icon>
              </v-list-item-icon>
              <v-list-item-title>Github</v-list-item-title>
            </v-list-item></a
          >

          <a
            href="https://www.linkedin.com/in/trevorvonhake/"
            class="icon-link"
            target="_blank"
            ><v-list-item>
              <v-list-item-icon>
                <v-icon>{{ LinkedIn }}</v-icon>
              </v-list-item-icon>
              <v-list-item-title>LinkedIn</v-list-item-title>
            </v-list-item></a
          >
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <v-content class="ma-0 pa-0">
      <home-content id="top"></home-content>
      <home-details id="aboutme"></home-details>
      <projects id="projects"></projects>
      <about-site id="aboutsite"></about-site>
    </v-content>
  </span>
</template>

<script>
import AboutSite from '../components/AboutSite.vue';
import HomeContent from '../components/HomeContent.vue';
import HomeDetails from '../components/HomeDetails.vue';
import Projects from '../components/Projects.vue';
import {
  mdiAccountCircle,
  mdiFolderMultipleOutline,
  mdiGithub,
  mdiInformation,
  mdiLinkedin,
} from '@mdi/js';

export default {
  name: 'home',
  components: {
    HomeContent,
    HomeDetails,
    Projects,
    AboutSite,
  },
  data: () => ({
    drawer: false,
    group: null,
    Github: mdiGithub,
    LinkedIn: mdiLinkedin,
    Folder: mdiFolderMultipleOutline,
    Account: mdiAccountCircle,
    Information: mdiInformation,
  }),
};
</script>

<style scoped>
.icon-link {
  color: inherit;
  text-decoration: none;
}
.icon-link:hover {
  color: midnightblue;
  text-decoration: none;
}
.custom-btn::before {
  color: transparent;
}

.custom-btn:hover {
  color: transparent;
}
</style>
