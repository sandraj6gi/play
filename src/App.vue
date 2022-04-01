<template>
  <v-app id="app">
    <v-main>
      <v-container>
        <v-card>
          <v-btn color="white"
                 x-large
                 @click="toggleVideo">
            {{this.buttonText}}
          </v-btn>
          <video-component
              :isSandra="this.isSandra">
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
  methods: {
    toggleVideo() {
      this.isSandra = !this.isSandra
      this.buttonText = this.isSandra ? "Watch a video of a cat" : "Watch a video of Sandra"
    }
  },
  data() {
    return {
      isSandra: true,
      buttonText: "Watch a video of cats"
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
}
.container {
  width: 83.33vw;
  height: 45vw;
  margin-top: -0.5vw;
  padding: 0 !important;
}
.v-btn {
  margin: 4vw 0 3vw 0;
}
.v-card {
  height: 100%;
  box-shadow: none !important;
  background-image: linear-gradient(to top, rgba(231,62,149,0), rgba(255,0,0,0.3));
}
</style>
