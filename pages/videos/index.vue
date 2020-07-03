<template>
  <div>
    <nuxt-child />
    <h1>Videos</h1>
    <div v-for="video in videos" :key="video.id">
      <nuxt-link :to="`/videos/${video.id}`">{{ video.title }}</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  asyncData(context) {
    return context.$axios
      .get("https://my-json-server.typicode.com/nurettinyakit/fake-json-api/items")
      .then(response => {
        console.log(response.data);
        return { videos: response.data };
      });
  },
  data() {
    return {
      posts: {},
      videos: [
        {
          id: 1,
          title: "First video."
        },
        {
          id: 2,
          title: "Second video."
        },
        {
          id: 20,
          title: "Latest video."
        }
      ]
    };
  }
};
</script>

<style></style>
