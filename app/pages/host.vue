<script setup lang="ts">
const host = useRoute().params.host
const { data: page } = await useAsyncData(`${host}`, () => {
    // Not 100% sure we have to get the first here, but I think
    // queryCollection returns a list, so we do need to get a single element.
    return queryCollection('content').path(`/host`).first()
})

// the remaining code is NOT in use as of right now, and may never be
/*
const os = ref("Detecting...")
const mdcVars = ref({ to: "https://github.com/Sanae6/SmoOnlineServer/releases"});

const getOS = (): string => {
    const userAgent = navigator.userAgent
    if (userAgent.includes("Win")) return "Windows"
    if (userAgent.includes("Mac")) return "MacOS"
    if (userAgent.includes("Linux")) return "Linux"
    return "Other"
}

onMounted(() => {
    os.value = getOS() || "Other"
    mdcVars.value.to = {
            "Linux": "https://github.com/Sanae6/SmoOnlineServer/releases/download/1.0.4/Server",
            "Windows": "https://github.com/Sanae6/SmoOnlineServer/releases/download/1.0.4/Server.exe",
        }[os.value] || "https://github.com/Sanae6/SmoOnlineServer/releases"

    console.log(os.value)
    console.log(mdcVars)
})
*/
</script>

<!--
Reference for this code:
https://content.nuxt.com/docs/files/markdown#display-markdown
-->
<template>
    <Headline :text="page?.title" />
    <ContentRenderer :value="page" />
</template>