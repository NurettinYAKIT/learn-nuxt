<template>
  <div>
    <nuxt-child />
    <h1>Videos</h1>
    <div v-for="video in videos" :key="video.id">
      <nuxt-link :to="`/videos/${video.id}`" >{{video.name}}</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      videos: [
        {
          id: 1,
          name: "First video."
        },
        {
          id: 2,
          name: "Second video."
        },
        {
          id: 20,
          name: "Latest video."
        }
      ]
    };
  }
};
</script>

<style>
</style>