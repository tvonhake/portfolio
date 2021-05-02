<template>
  <v-container
    fluid
    fill-height
    grid-list-lg
    class="home-details"
    style="max-height: 100vh; max-width: 100vw"
  >
    <v-layout justify-center align-center column pa-5>
      <v-row dense class="row1">
        <v-flex xs12 class="text-xs-center white--text display-1"
          >About Me</v-flex
        >
      </v-row>
      <v-row dense class="row2">
        <v-btn
          @click="
            skills = true;
            education = false;
            learnmore = false;
          "
          dark
          color="transparent"
          >My Skills</v-btn
        ><v-btn
          @click="
            skills = false;
            education = true;
            learnmore = false;
          "
          dark
          color="transparent"
          >Education</v-btn
        ><v-btn
          @click="
            skills = false;
            education = false;
            learnmore = true;
          "
          dark
          color="transparent"
          >Learn More</v-btn
        >
      </v-row>
      <div v-if="skills">
        <v-row>
          <v-tooltip top>
            <template v-slot:activator="{ on, attrs }">
              <v-icon
                x-large
                v-bind="attrs"
                v-on="on"
                color="yellow lighten-2"
                >{{ Javascript }}</v-icon
              >
            </template>
            <span>Javascript</span>
          </v-tooltip>
          <v-tooltip top>
            <template v-slot:activator="{ on, attrs }">
              <v-icon
                x-large
                v-bind="attrs"
                v-on="on"
                color="light-blue lighten-3"
                >{{ React }}</v-icon
              >
            </template>
            <span>React JS</span>
          </v-tooltip>
          <v-tooltip top>
            <template v-slot:activator="{ on, attrs }">
              <v-icon x-large v-bind="attrs" v-on="on" color="red lighten-1">{{
                Ruby
              }}</v-icon>
            </template>
            <span>Ruby</span>
          </v-tooltip>
          <v-tooltip top>
            <template v-slot:activator="{ on, attrs }">
              <v-icon x-large v-bind="attrs" v-on="on" color="red darken-3">{{
                RubyOnRails
              }}</v-icon>
            </template>
            <span>Ruby on Rails</span>
          </v-tooltip>
          <v-tooltip top>
            <template v-slot:activator="{ on, attrs }">
              <v-icon
                x-large
                v-bind="attrs"
                v-on="on"
                color="orange darken-4"
                >{{ HTML5 }}</v-icon
              >
            </template>
            <span>HTML5</span>
          </v-tooltip>
          <v-tooltip top>
            <template v-slot:activator="{ on, attrs }">
              <v-icon x-large v-bind="attrs" v-on="on" color="blue darken-2">{{
                CSS
              }}</v-icon>
            </template>
            <span>CSS3</span>
          </v-tooltip>
        </v-row>
        <v-row class="mt-10">
          <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
              <v-icon
                x-large
                v-bind="attrs"
                v-on="on"
                color="deep-purple lighten-1"
                >{{ Bootstrap }}</v-icon
              >
            </template>
            <span>Bootstrap & React Bootstrap</span>
          </v-tooltip>
          <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
              <v-icon x-large v-bind="attrs" v-on="on" color="teal lighten-3">{{
                Semantic
              }}</v-icon>
            </template>
            <span>Semantic UI</span>
          </v-tooltip>
          <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
              <v-icon x-large v-bind="attrs" v-on="on" color="green darken-1">{{
                Vue
              }}</v-icon>
            </template>
            <span>Vue</span>
          </v-tooltip>
          <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
              <v-icon
                x-large
                v-bind="attrs"
                v-on="on"
                color="light-blue lighten-1"
                >{{ VSCode }}</v-icon
              >
            </template>
            <span>Visual Studio Code</span>
          </v-tooltip>
          <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
              <v-icon x-large v-bind="attrs" v-on="on" color="white">{{
                GitHub
              }}</v-icon>
            </template>
            <span>GitHub</span>
          </v-tooltip>
          <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
              <v-icon
                x-large
                v-bind="attrs"
                v-on="on"
                color="deep-orange darken-1"
                >{{ MSO }}</v-icon
              >
            </template>
            <span>Microsoft Office</span>
          </v-tooltip>
        </v-row>
      </div>
      <div class="mt-n16" v-if="education">
        <v-row class="dpl">
          <p class="subheading my-10 white--text display-0">
            Devpoint Labs Full Stack Web Development - April 2021
          </p>
        </v-row>
        <v-row class="uofu">
          <p class="subheading white--text display-0">
            University of Utah BS Psychology - May 2022
          </p>
        </v-row>
      </div>
      <div class="mt-n8" v-if="learnmore">
        <v-row>
          <v-btn
            x-large
            color="transparent"
            depressed
            dark
            href="https://www.linkedin.com/in/trevorvonhake/"
            target="_blank"
          >
            <v-icon x-large color="blue-grey lighten-2">{{ LinkedIn }}</v-icon
            >LinkedIn
          </v-btn>
        </v-row>
        <v-row mt-16>
          <v-btn
            x-large
            color="transparent"
            depressed
            dark
            href="/https://github.com/tvonhake"
            target="_blank"
            class="git-btn"
          >
            <v-icon x-large>{{ GitHub }}</v-icon
            >GitHub
          </v-btn>
        </v-row>
      </div>
      <v-spacer />
    </v-layout>
  </v-container>
</template>

<script>
import {
  mdiBootstrap,
  mdiGithub,
  mdiLanguageCss3,
  mdiLanguageHtml5,
  mdiLanguageJavascript,
  mdiLanguageRuby,
  mdiLanguageRubyOnRails,
  mdiLinkedin,
  mdiMicrosoftOffice,
  mdiMicrosoftVisualStudioCode,
  mdiReact,
  mdiSemanticWeb,
  mdiVuejs,
  mdiVuetify,
} from '@mdi/js';

export default {
  name: 'HomeDetails',
  data: () => ({
    skills: true,
    education: false,
    learnmore: false,
    Javascript: mdiLanguageJavascript,
    React: mdiReact,
    Ruby: mdiLanguageRuby,
    RubyOnRails: mdiLanguageRubyOnRails,
    Vue: mdiVuejs,
    Vuetify: mdiVuetify,
    Bootstrap: mdiBootstrap,
    Semantic: mdiSemanticWeb,
    GitHub: mdiGithub,
    VSCode: mdiMicrosoftVisualStudioCode,
    HTML5: mdiLanguageHtml5,
    CSS: mdiLanguageCss3,
    MSO: mdiMicrosoftOffice,
    LinkedIn: mdiLinkedin,
  }),
};
</script>

<style scoped>
.home-details {
  background-color: rgb(54, 54, 54);
  width: 100% !important;
  height: 100%;
}
.v-icon {
  margin: 0px 10px 0px 10px;
}
.div {
  margin: 0;
  padding: 0;
}
.git-btn {
  padding-right: 100px;
}
.row1 {
  max-height: 100px;
}
.v-flex {
  max-height: 100px;
}
.row2 {
  max-height: 100px;
  align-content: center;
  justify-content: center;
  margin: 0 0 100px 0;
}
.v-btn {
  margin: 5px 0 5px 0;
}
.uofu {
  background: url('https://i.imgur.com/HMJCxWB.png');
  background-position-x: right;
  background-position-y: center;
  background-size: 100px;
  background-repeat: no-repeat;
  align-content: center;
  justify-content: center;
  width: 45vw;
  height: 100%;
  margin: 0px 0 10px 0;
  padding: 0 50px 0 0;
}
.dpl {
  background: url('https://i.imgur.com/Y0XPXwi.png');
  background-position-x: right;
  background-position-y: center;
  background-size: 100px;
  background-repeat: no-repeat;
  align-content: center;
  justify-content: center;
  width: 45vw;
  height: 100%;
  margin: -50px 0 10px 0;
  padding: 0 90px 0 0;
}
</style>
