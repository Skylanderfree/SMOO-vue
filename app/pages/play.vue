<script setup lang="ts">

</script>

<template>
  <div>
    <div class="rounded-lg border border-default p-4 w-full mt-12">
      <UCollapsible class="flex flex-col gap-2">
        <UButton
          class="group"
          label="Playing on a hacked Nintendo Switch"
          color="neutral"
          variant="subtle"
          trailing-icon="i-lucide-chevron-down"
          :ui="{
            trailingIcon: 'group-data-[state=open]:rotate-180 transition-transform duration-200',
          }"
          block
        />

        <template #content>
          <div class="px-4 pb-4">
            <p class="text-neutral-400 text-sm italic">
              Instructions for hacked Switch here
            </p>
          </div>
        </template>
      </UCollapsible>
    </div>
    <div class="rounded-lg border border-default p-4 w-full mt-8">
      <UCollapsible class="flex flex-col gap-2">
        <UButton
          class="group"
          label="Playing on a Emulator"
          color="neutral"
          variant="subtle"
          trailing-icon="i-lucide-chevron-down"
          :ui="{
            trailingIcon: 'group-data-[state=open]:rotate-180 transition-transform duration-200',
          }"
          block
        />

        <template #content>
          <div class="flex flex-col gap-4 mt-4 px-4 pb-4">
            <UCollapsible class="flex flex-col gap-2">
              <UButton
                class="group"
                label="Ryujinx"
                color="neutral"
                variant="subtle"
                trailing-icon="i-lucide-chevron-down"
                :ui="{
                  trailingIcon: 'group-data-[state=open]:rotate-180 transition-transform duration-200',
                }"
                block
              />
              <template #content>
                <div class="px-4 pb-2">
                  <p class="text-neutral-400 text-sm italic">
                    Ryujinx specific instructions here
                  </p>
                </div>
              </template>
            </UCollapsible>
            <UCollapsible class="flex flex-col gap-2">
              <UButton
                class="group"
                label="Yuzu / Suyu / Sudachi"
                color="neutral"
                variant="subtle"
                trailing-icon="i-lucide-chevron-down"
                :ui="{
                  trailingIcon: 'group-data-[state=open]:rotate-180 transition-transform duration-200',
                }"
                block
              />
              <template #content>
                <div class="px-4 pb-2">
                  <p class="text-neutral-400 text-sm italic">
                    Yuzu and related emulators instructions here
                  </p>
                </div>
              </template>
            </UCollapsible>
          </div>
        </template>
      </UCollapsible>
    </div>
    <div class="rounded-lg border border-default p-4 w-full mt-8">
      <UCollapsible class="flex flex-col gap-2">
        <UButton
          class="group"
          label="Compiling the mod from source (advanced)"
          color="neutral"
          variant="subtle"
          trailing-icon="i-lucide-chevron-down"
          :ui="{
            trailingIcon: 'group-data-[state=open]:rotate-180 transition-transform duration-200',
          }"
          block
        />

        <template #content>
          <div class="px-4 pb-4">
            <p class="text-neutral-400 text-sm italic">
              Instructions for compiling from source here
            </p>
          </div>
        </template>
      </UCollapsible>
    </div>
  </div>
</template>

<style scoped>

</style>
