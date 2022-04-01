<template>
  <v-app id="app">
    <v-main>
      <v-container>
        <v-card>
          <v-card-title>Hello</v-card-title>
          <video-component>
          </video-component>
        </v-card>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import VideoComponent from "@/components/VideoComponent";
export default {
  name: 'App',
  components: {
    VideoComponent

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
