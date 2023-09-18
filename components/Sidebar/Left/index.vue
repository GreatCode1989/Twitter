<template>
  <div class="h-screen flex flex-col">
    <div
      class="p-2 my-2 hover:bg-blue-50 rounded-full w-min"
      :class="defaultTransition"
    >
      <nuxt-link to="/">
        <div class="w-8 h-8"><LogoTwitter /></div
      ></nuxt-link>
    </div>
    <SidebarLeftTab active>
      <template v-slot:icon>
        <HomeIcon />
      </template>
      <template v-slot:name> Home </template>
    </SidebarLeftTab>
  </div>
</template>

<script setup>
import { HomeIcon } from "@heroicons/vue/20/solid";

const { defaultTransition } = useTailwindConfig();
</script>
