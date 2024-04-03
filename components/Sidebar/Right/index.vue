<template>
  <div class="flex flex-col">
    <!-- Preview Card: What's happening -->
    <div>
      <LayoutPreviewCard title="What's happening">
        <SidebarRightItem v-for="item in whatsHappeningItems" :key="item.id">
          <div>
            <h4 class="font-bold text-gray-800 text-lg dark:text-white">
              {{ item.title }}
            </h4>
            <p class="text-sm text-gray-400">{{ item.count }}</p>
          </div>
        </SidebarRightItem>
      </LayoutPreviewCard>
    </div>

    <!-- Preview Card: Who to follow -->
    <div>
      <LayoutPreviewCard title="Who to follow">
        <SidebarRightItem v-for="item in whoToFollow" :key="item.id">
          <div class="flex justify-between items-center p-2">
            <div class="flex items-center gap-3">
              <NuxtImg
                class="w-min h-10 rounded-full"
                src="avatar.png"
                alt=""
              />
              <div>
                <p class="font-bold">{{ item.name }}</p>
                <p class="text-sm">{{ item.handle }}</p>
              </div>
            </div>
            <button
              class="py-2 px-4 text-white bg-blue-400 rounded-full font-semibold hover:bg-blue-400/80 dark:bg-white dark:text-black"
              :class="defaultTransition"
            >
              Follow
            </button>
          </div>
        </SidebarRightItem>
      </LayoutPreviewCard>
    </div>
  </div>
</template>

<script setup lang="ts">
const { defaultTransition } = useTailwindConfig()
const whatsHappeningItems = ref([
  {
    id: 1,
    title: "SpaceX",
    count: "18.8k Tweets",
  },
  {
    id: 2,
    title: "#CodingIsFun",
    count: "18.8k Tweets",
  },
  {
    id: 3,
    title: "#artforall",
    count: "18.8k Tweets",
  },
]);

const whoToFollow = ref([
  {
    id: 1,
    name: "Putin",
    handle: "@putin555",
  },
  {
    id: 2,
    name: "Putin",
    handle: "@putin555",
  },
  {
    id: 3,
    name: "Putin",
    handle: "@putin555",
  },
]);
</script>

<style scoped></style>
