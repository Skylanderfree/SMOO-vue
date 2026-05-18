<script setup>
import { ref, onMounted } from 'vue'

const isLinux = ref(false)
const isWindows = ref(false)
// default to unsupported
const isUnsupported = ref(true)

onMounted(() => {
    const platform = navigator.userAgentData?.platform || navigator.platform || ''
    isLinux.value = platform.toLowerCase().includes('linux')
    isWindows.value = platform.toLowerCase().includes('windows')
    isUnsupported.value = !(isLinux.value || isWindows.value)
})

const host = useRoute().params.host
const { data: page } = await useAsyncData(`${host}`, () => {
    // Not 100% sure we have to get the first here, but I think
    // queryCollection returns a list, so we do need to get a single element.
    return queryCollection('content').path(`/host`).first()
})
</script>

<!--
Reference for this code:
https://content.nuxt.com/docs/files/markdown#display-markdown
-->
<template>
    <Headline :text="page?.title" />
    
    <!-- Render the right download button -->
    <template>
            <ClientOnly>
                <!-- TODO: figure out how to get this to let the user know their device may not be supported. -->

                <div v-if="isUnsupported" class="pb-4 place-items-center">
                    <UAlert class="mb-4" color="warning" title="Unsupported" description="This device may not be supported for hosting a server." />
                    <UButton block size="xl" icon="i-lucide-rocket" color="warning" variant="soft" to="https://github.com/Sanae6/SmoOnlineServer/releases/latest/">Official Server Versions</UButton>
                </div>

                <div v-else class="pb-8 md:px-20 lg:px-100 justify-center">
                    <UButton v-if="isLinux" block size="xl" icon="i-lucide-rocket" to="https://github.com/Sanae6/SmoOnlineServer/releases/latest/download/Server">Quick Install - Linux</UButton>
                    <UButton v-else-if="isWindows" size="xl" icon="i-lucide-rocket" to="https://github.com/Sanae6/SmoOnlineServer/releases/latest/download/Server.exe">Quick Install - Windows</UButton>
                    <p v-else><em>An error occured while determining your OS.</em></p>
                </div>
            </ClientOnly>
    </template>

    <!-- Render page contents -->
    <ContentRenderer :value="page" />
</template>