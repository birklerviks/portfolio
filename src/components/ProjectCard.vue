<script setup lang="ts">
const props = defineProps(['flip'])
</script>
<template>
    <div :class="`pt-4 pb-16 flex gap-12 ${props.flip ? 'lg:flex-row-reverse flex-col' : 'lg:flex-row flex-col'}`">
        <div class="lg:w-1/2 flex flex-col gap-2 text-zinc-300">
            <h2 class="text-2xl font-bold text-white"><slot name="header"></slot></h2>
            <slot name="description"></slot>
        </div>
        <div class="lg:w-1/2 aspect-[16/9]">
            <slot name="content"></slot>
        </div>
    </div>
</template>