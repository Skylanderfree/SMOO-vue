
<script setup lang="ts">
definePageMeta({
  layout: 'docs'
})

const route = useRoute()

const { data: page } = await useAsyncData(route.path, () =>
  queryCollection('content')
    .path(route.path)
    .first()
)

if (!page.value) {
  throw createError({
    statusCode: 404,
    statusMessage: 'Page not found'
  })
}
</script>

<template>
  <div>
    <Headline :text="page.title" />

    <ContentRenderer :value="page" />
  </div>
</template>