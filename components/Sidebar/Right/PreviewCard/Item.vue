<template>
    <div class="p-3 cursor-pointer hover:bg-gray-100 border-b" :class="wrapperClasses">
<slot></slot>
    </div>
</template>

<script setup>
const { twitterBorderColor, defaultTransition } = useTailwindConfig();

const wrapperClasses = computed(() => `${twitterBorderColor} ${defaultTransition}`)
</script>

