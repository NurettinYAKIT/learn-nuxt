<template>
  <div>
    <nuxt-child :video="video" />
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
  },
  computed: {
    video() {
      return this.videos.find(v => v.id == this.$route.params.id);
    }
  }
};
</script>

<style></style>
