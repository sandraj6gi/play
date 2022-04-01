<template>
  <v-app id="app">
    <v-main>
      <v-container>
        <v-card>
          <v-btn
              @click="isSandra = !isSandra">
            Button
          </v-btn>
          <video-component :isSandra="this.isSandra">
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
  },
  data() {
    return {
      isSandra: true
    };
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

.container {
  width: 83.33vw;
  height: 45vw;
  margin-top: 5vw;
}
.v-card {
  height: 100%;
  padding-top: 2vw;
}
</style>
