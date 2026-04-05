<script setup lang="ts">
const { data: home } = await useAsyncData(() => queryCollection("content").path("/").first());

useSeoMeta({
  title: home.value?.title,
  description: home.value?.description,
});
</script>

<template>
  <div class="container">
    <div class="text-center">
      <h3>Welcome to the official Super Mario Odyssey Online Website</h3>
      <iframe
        width="818"
        height="460"
        src="https://www.youtube.com/embed/nXxnhvP_LEI"
        title="Super Mario Odyssey Online Multiplayer is OUT NOW"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        referrerpolicy="strict-origin-when-cross-origin"
        allowfullscreen
      />
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

