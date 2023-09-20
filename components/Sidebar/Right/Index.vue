<template>
  <div class="flex flex-col">
    <!-- Preview Card: What's happening -->
    <SidebarRightPreviewCard title="What's happening">
      <SidebarRightPreviewCardItem
        v-for="whatsHappening in whatsHappeningItems"
        :key="whatsHappening.title"
      >
        <div>
          <h2 class="font-bold text-gray-900 text-md">{{ whatsHappening.title }}</h2>
          <p class="text-xs text-gray-400">{{ whatsHappening.count }}</p>
        </div>
      </SidebarRightPreviewCardItem>
    </SidebarRightPreviewCard>
    <!-- Preview Card: Who to follow -->
    <SidebarRightPreviewCard title="Who to follow">
        <SidebarRightPreviewCardItem
        v-for="whoToFollow in whoToFollowItems"
        :key="whoToFollow.name"
      >
        <div class="flex flex-row items-center justify-between p-2">
          <div class="flex flex-row">
            <img class="w-10 h-10 rounded-full" :src="whoToFollow.image" :alt="whoToFollow.name">
            <div class="flex flex-col ml-2">
                <h1 class="font-bold text-gray-900 text-sm">{{ whoToFollow.name }}</h1>
                <p class="text-xl text-gray-400">{{ whoToFollow.handle }}</p>
            </div>
          </div>
          <div class="flex h-full">
            <button class="px-4 py-2 font-bold text-xs rounded-full bg-blue-300 text-white">Follow</button>
          </div>
        </div>
      </SidebarRightPreviewCardItem>
    </SidebarRightPreviewCard>
  </div>
</template>

<script setup>
const whatsHappeningItems = ref([
  {
    title: "SpaceX",
    count: "18.8k Tweets",
  },
  {
    title: "CodingIsFan",
    count: "8.8k Tweets",
  },
  {
    title: "artforall",
    count: "1.8k Tweets",
  },
]);

const whoToFollowItems = ref([
    {
        name:'Jo Jones',
        handle: '@JoJones',
        image: 'https://picsum.photos/200/200'
    },
    {
        name:'Jack DeJohnnette',
        handle: '@JackDeJohnnette',
        image: 'https://picsum.photos/200/201'
    },
    {
        name:'Buddy Rich',
        handle: '@BuddyRich',
        image: 'https://picsum.photos/200/202'
    }
])
</script>
