<template>
  <div
    class="m-2 border overflow-hidden rounded-2xl bg-gray-50"
    :class="twitterBorderColor"
  >
    <h1 class="p-3 text-xl font-extrabold text-gray-800 border-b">
      {{ props.title }}
    </h1>
    <slot></slot>

    <div
      class="p-3 text-sm text-blue-400 cursor-pointer hover:bg-gray-100"
      :class="defaultTransition"
    >
      Show more
    </div>
  </div>
</template>

<script setup>
const { twitterBorderColor, defaultTransition } = useTailwindConfig();

const props = defineProps({
  title: {
    type: String,
    required: true,
  },
});
</script>
