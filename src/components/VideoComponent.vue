<template>
  <v-container>
    <video

        style="width: 100%"
        controls
        autoplay="false"
        loop="false"
    >
      <source :src="videoLink" type="video/webm" />
    </video>
  </v-container>

</template>

<script>

export default {
  name: "VideoComponent",
  data() {
    return {
      videoLink: "https://www.youtube.com/watch?v=xbs7FT7dXYc"
    }
  }
}
</script>

<style scoped>

</style>