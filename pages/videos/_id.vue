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
  },
  computed: {
    video() {
      return this.videos.find(v => v.id == this.$route.params.id);
    }
  }
};
</script>

<style></style>
