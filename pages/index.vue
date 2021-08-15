<template>
  <div>
    <ul class="flex flex-wrap justify-between">
      <template v-for="(launch, index) in launches">
        <li
          class="
            max-w-sm
            w-full
            border-2
            rounded-md
            h-72
            flex flex-col
            overflow-hidden
            mb-5
          "
          v-if="launch.links.patch.small"
          v-bind:key="index"
        >
          <NuxtLink
            :to="`/${launch.name.split('/').join('-').replace(/ /g, '')}/${
              launch.id
            }`"
          >
            <div class="flex justify-center">
              <img
                class="w-32 h-32 mt-4"
                v-bind:src="launch.links.patch.small"
                alt="rocket-launch"
              />
            </div>
            <div class="p-4">
              <h1 v-if="launch.name" class="font-bold text-xl">
                {{ launch.name }}
              </h1>
              <p v-if="launch.details">
                {{ launch.details }}
              </p>
            </div>
          </NuxtLink>
        </li>
      </template>
    </ul>
  </div>
</template>

<script>
export default {
  layout: 'BaseLayout',
  async asyncData({ params, $axios, $config }) {
    const launches = await $axios.$get(`${$config.spaceXBaseURL}/launches`)
    return { launches }
  },
}
</script>
