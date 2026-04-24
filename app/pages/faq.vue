<script setup>
const faq = useRoute().params.faq
const { data: page } = await useAsyncData(`${faq}`, () => {
  // Not 100% sure we have to get the first here, but I think
  // queryCollection returns a list, so we do need to get a single element.
  return queryCollection('content').path(`/faq`).first()
})
</script>

<template>
  <!--
  Reference for this code:
  https://content.nuxt.com/docs/files/markdown#display-markdown
  -->
  <ContentRenderer :value="page" />
</template>
