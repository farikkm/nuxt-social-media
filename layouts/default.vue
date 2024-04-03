<script setup lang="ts">
const darkMode = ref(false);
</script>

<template>
  <div :class="{ dark: darkMode }">
    <div class="bg-white dark:bg-dim-900">
      <div class="min-h-full">
        <div
          class="grid grid-cols-12 mx-auto sm:px-6 lg:max-w-7xl lg:px-8 lg:gap-5"
        >
          <!-- Left Sidebar -->

          <!-- TODO: Remove the border -->
          <div
            class="hidden md:block border-blue-400 md:col-span-1 xl:col-span-2"
          >
            <div class="sticky top-0">
              <SidebarLeft />
            </div>
          </div>

          <!-- Main Content -->
          <main class="col-span-12 bg-blue-500/20 md:col-span-8 xl:col-span-6">
            <slot></slot>
          </main>

          <!-- Right Sidebar -->
          <div
            class="hidden md:block md:col-span-3 xl:col-span-4"
          >
            <div class="sticky top-0">
              <SidebarRight />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
