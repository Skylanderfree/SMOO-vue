<!-- Taken from the Nuxt documentation, https://content.nuxt.com/docs/files/markdown -->
<script setup>
const props = defineProps({ type: { type: String } })

const alertClass = computed(() => {
    return {
        warning: 'bg-yellow-100 border-orange-200 dark:bg-yellow-800 dark:border-yellow-800',
        info: 'bg-blue-100 border-blue-200 dark:bg-blue-900 dark:border-blue-800',
        success: 'bg-green-100 border-green-200 dark:bg-green-900 dark:border-green-800',
    }[props.type]
})
</script>

<template>
    <div class="text-black p-2 border dark:text-white rounded" :class="alertClass">
        <slot mdc-unwrap="p" />
    </div>
</template>
