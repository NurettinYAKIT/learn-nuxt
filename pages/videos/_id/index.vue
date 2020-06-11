<template>
  <div>
    <h1>Video Details</h1>
    <h3>{{video.name}}</h3>
    <nuxt-link :to="`/videos/${video.id}/edit`">
      <button>Edit</button>
    </nuxt-link>
  </div>
</template>

<script>
export default {
  props: ["video"]
};
</script>
<style>
</style>