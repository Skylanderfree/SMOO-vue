<script setup>
const compatibility = useRoute().params.compatibility
const { data: page } = await useAsyncData(`${compatibility}`, () => {
    // See faq.vue for `.first()` thoughts.
  return queryCollection('content').path(`/compatibility`).first()
})
</script>

<template>
  <!--
  Reference for this code:
  https://content.nuxt.com/docs/files/markdown#display-markdown
  -->
  <ContentRenderer :value="page" />
</template>
