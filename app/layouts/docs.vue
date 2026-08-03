<script setup lang="ts">

const items = [
  {
    label: 'Setup',
    children: [
      {
        label: 'Prerequisites',
        to: '/setup/prerequisites'
      },
      {
        label: 'Installation',
        to: '/setup/installation'
      }
    ]
  },
  {
    label: 'Playing',
    children: [
      {
        label: 'Play',
        to: '/play'
      }
    ]
  },
  {
    label: 'Server',
    children: [
      {
        label: 'Hosting',
        to: '/server/hosting'
      }
    ]
  }
]

</script>

<template>
  <div class="min-h-screen">
    <AppNavBar />

    <div class="flex">
      <aside class="w-64 border-r p-4">
        <UNavigationMenu
          :items="items"
          orientation="vertical"
        />
      </aside>

      <main class="flex-1 p-6">
        <slot />
      </main>
    </div>
  </div>
</template>