<template>
  <v-app id="app">
    <v-main>
      <v-container>
        <v-card>
          <v-btn
              @click="toggleVideo">
            Button {{this.buttonText}}
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
  methods: {
    toggleVideo() {
      this.isSandra = !this.isSandra
      this.buttonText = this.isSandra ? "Watch a video of a cat" : "Watch a video of Sandra"
    }
  },
  data() {
    return {
      isSandra: true,
      buttonText: "Watch a video of a cat"
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
