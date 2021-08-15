<template>
  <div>
    <h1 class="text-3xl font-bold mb-2">{{ launch.name }}</h1>
    <iframe
      width="100%"
      height="500"
      :src="`https://www.youtube.com/embed/${launch.links.youtube_id}`"
      frameborder="0"
      allowfullscreen
    ></iframe>
    <p class="mt-2">{{ launch.details }}</p>
  </div>
</template>

<script>
export default {
  layout: 'BaseLayout',
  async asyncData({ params, $axios, $config }) {
    const launch = await $axios.$get(
      `${$config.spaceXBaseURL}/launches/${params.launchId}`
    )
    return { params, launch }
  },
}
</script>
<style lang="scss" scoped></style>
