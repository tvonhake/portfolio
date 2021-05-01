<template>
  <v-container fluid fill-height class="home-content" style="max-height: 100vh">
    <v-layout justify-center align-center column pa-5>
      <div class="display-4 font-weight-black white--text text-xs-center">
        FULL STACK
      </div>
      <div class="display-4 font-weight-black white--text text-xs-center mb-3">
        SOFTWARE ENGINEER
      </div>
      <div class="display-1 font-weight-bold white--text text-xs-center">
        Passionate about making beautiful applications from start to finish
      </div>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: 'HomeContent',
};
</script>

<style scoped>
.home-content {
  background: url('http://source.unsplash.com/Dx9fxRylvMk');
  background-size: cover;
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
}
</style>
