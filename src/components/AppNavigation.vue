<template>
  <span>
    <v-tool-bar color="transparent" flat class="pa-0" dark>
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
    </v-tool-bar>

    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-list nav dense>
        <v-list-item-group
          v-model="group"
          active-class="blue-grey--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-icon>
              <v-icon>{{ Account }}</v-icon>
            </v-list-item-icon>
            <v-list-item-title>About Me</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-icon>
              <v-icon>{{ Folder }}</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Projects</v-list-item-title>
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

          <v-list-item>
            <v-list-item-icon>
              <v-icon>{{ Information }}</v-icon>
            </v-list-item-icon>
            <v-list-item-title>About This Site</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </span>
</template>

<script>
import {
  mdiAccountCircle,
  mdiFolderMultipleOutline,
  mdiGithub,
  mdiInformation,
  mdiLinkedin,
} from '@mdi/js';

export default {
  name: 'AppNavigation',
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
