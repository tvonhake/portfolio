<template>
  <span>
    <v-app-bar color="transparent" flat class="pa-0" light>
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>

      <v-toolbar-title>Trevor von Hake</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>{{ svgPath1 }}</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>{{ svgPath2 }}</v-icon>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-list nav dense>
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-account</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Account</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </span>
</template>

<script>
import { mdiGithub, mdiLinkedin } from '@mdi/js';

export default {
  name: 'AppNavigation',
  data: () => ({
    drawer: false,
    group: null,
    svgPath1: mdiGithub,
    svgPath2: mdiLinkedin,
  }),
};
</script>

<style scoped></style>
