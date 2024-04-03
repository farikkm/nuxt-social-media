<script setup lang="ts">
import { HomeIcon, } from "@heroicons/vue/solid";
import { BellIcon, BookmarkIcon, DocumentTextIcon, DotsCircleHorizontalIcon, HashtagIcon, InboxIcon, UserIcon } from '@heroicons/vue/outline'

const { defaultTransition } = useTailwindConfig();
</script>

<template>
  <div>
    <div class="h-screen flex flex-col">
      <div
        class="p-2 my-2 rounded-full w-min hover:bg-blue-50 dark:hover:bg-white/10"
        :class="defaultTransition"
      >
        <NuxtLink to="/">
          <div class="w-12 h-12">
            <LogoTwitter />
          </div>
        </NuxtLink>
      </div>

      <div class="space-y-3 mt-3">
        <SidebarLeftTab name="Home" href="/">
          <HomeIcon />
        </SidebarLeftTab>
        <SidebarLeftTab name="Explore" href="/explore">
          <HashtagIcon />
        </SidebarLeftTab>
        <SidebarLeftTab name="Notifications" href="/notifications">
          <BellIcon />
        </SidebarLeftTab>
        <SidebarLeftTab name="Messages" href="/messages">
          <InboxIcon />
        </SidebarLeftTab>
        <SidebarLeftTab name="Bookmarks" href="/bookmarks">
          <BookmarkIcon />
        </SidebarLeftTab>
        <SidebarLeftTab name="Lists" href="/lists">
          <DocumentTextIcon />
        </SidebarLeftTab>
        <SidebarLeftTab name="Profile" href="/profile">
          <UserIcon />
        </SidebarLeftTab>
        <SidebarLeftTab name="More" href="/more">
          <DotsCircleHorizontalIcon />
        </SidebarLeftTab>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
