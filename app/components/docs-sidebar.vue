<script setup lang="ts">
const { data: navigation } = await useAsyncData(() =>
  queryCollectionNavigation('docs')
)
</script>

<template>
  <aside class="w-72 border-r p-4">
    <UNavigationMenu
      :items="navigation || []"
      orientation="vertical"
    />
  </aside>
</template>