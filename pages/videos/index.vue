<template>
  <div>
    <h1>Videos</h1>
    <div v-for="video in videos" :key="video.id">{{video.name}}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      videos: [
        {
          id: 16,
          name: "First video."
        },
        {
          id: 17,
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