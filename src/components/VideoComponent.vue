<template>
  <div>
    <iframe
        v-if="!isSandra"
        :src="videoLink"
        allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen>
    </iframe>
    <iframe
        v-if="isSandra"
        :src="videoLinkSandra"
        allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen>
    </iframe>
  </div>
</template>

<script>

export default {
  name: "VideoComponent",
  props: {
    isSandra: Boolean
  },
  data() {
    return {
      videoLinkSandra: "https://www.youtube.com/embed/tndAVl6iGnk",
      videoLink: "https://www.youtube.com/embed/eX2qFMC8cFo?autoplay=1"
    }
  },
}
</script>

<style scoped>

iframe {
  width: 50vw;
  height: 28vw;
  border: none;
}

</style>