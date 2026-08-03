<script setup lang="ts">
const play = useRoute().params.play
const { data: page } = await useAsyncData(`${play}`, () => {
    // Not 100% sure we have to get the first here, but I think
    // queryCollection returns a list, so we do need to get a single element.
    return queryCollection('content').path(`/docs/play`).first()
})

</script>

<!--
Reference for this code:
https://content.nuxt.com/docs/files/markdown#display-markdown
-->
<template>
    <Headline :text="page?.title" />
    <ContentRenderer :value="page" />
</template>