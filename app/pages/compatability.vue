<script setup>
const compatability = useRoute().params.compatability
const { data: page } = await useAsyncData(`${compatability}`, () => {
    // See faq.vue for `.first()` thoughts.
  return queryCollection('content').path(`/compatability`).first()
})
</script>

<template>
  <!--
  Reference for this code:
  https://content.nuxt.com/docs/files/markdown#display-markdown
  -->
  <ContentRenderer :value="page" />
</template>
