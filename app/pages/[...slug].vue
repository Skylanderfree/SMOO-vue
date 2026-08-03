<script setup lang="ts">

const route = useRoute()

const { data: page } = await useAsyncData(route.path, () =>
  queryCollection('content')
    .where('stem', '=', route.path.replace('/', ''))
    .first()
)

console.log(page.value)

if (!page.value) {
  throw createError({
    statusCode: 404,
    statusMessage: `Content not found: ${route.path}`
  })
}

</script>

<template>
  <Headline :text="page.title" />

  <ContentRenderer :value="page" />
</template>