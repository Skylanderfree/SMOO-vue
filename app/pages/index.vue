<script setup lang="ts">
const { data: home } = await useAsyncData(() => queryCollection("content").path("/").first());

useSeoMeta({
  title: home.value?.title,
  description: home.value?.description,
});
</script>

<template>
  <div>
    <div class="mx-auto max-w-xl">
      <h2 class="mb-4 text-center">
        Welcome to the official Super Mario Odyssey Online Website
      </h2>
      <div class="aspect-video mb-4">
        <iframe
          class="size-full"
          src="https://www.youtube.com/embed/nXxnhvP_LEI"
          title="Super Mario Odyssey Online Multiplayer is OUT NOW"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
          referrerpolicy="strict-origin-when-cross-origin"
          allowfullscreen
        />
      </div>
    </div>
    <ContentRenderer
      v-if="home"
      :value="home"
    />
    <div v-else>
      Home not found
    </div>
  </div>
</template>
