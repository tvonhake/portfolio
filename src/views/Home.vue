<template>
  <span class="ma-0 pa-0">
    <home-content class="ma-0 pa-0"></home-content>
    <home-details></home-details>
    <projects class="ma-0 pa-0"></projects>
  </span>
</template>

<script>
import HomeContent from '../components/HomeContent.vue';
import HomeDetails from '../components/HomeDetails.vue';
import Projects from '../components/Projects.vue'

export default {
  name: 'home',
  components: {
    HomeContent,
    HomeDetails,
    Projects,
  },
};
</script>
