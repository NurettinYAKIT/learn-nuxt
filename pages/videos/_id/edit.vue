<template>
  <div>
    <h1>Editing the video</h1>
    <h3>{{ video.name }}</h3>
    <nuxt-link :to="`/videos/${video.id}`">
      <button>Back to the video</button>
    </nuxt-link>
  </div>
</template>

<script>
export default { props: ["video"] };
</script>

<style></style>
