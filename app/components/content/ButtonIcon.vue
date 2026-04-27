<script setup>
defineProps({
    path: {
        type: String,
        default: "a.png"
    },
    description: {
        type: String,
        default: "A controller icon."
    },
    size: {
        type: String,
        default: "6"
    },
})

const defaultClass = `w-${size} h-${size} inline`
const publicPath = `/img/${path}`
</script>

<!-- Do NOT use this component yet. It's very much a work-in-progress -->

<template>
    <NuxtImg :src="publicPath" :class="defaultClass"></NuxtImg>
</template>
