<template>
  <div
    class="p-3 border-b cursor-pointer hover:bg-gray-100 dark:text-white dark:hover:bg-dim-300"
    :class="[defaultTransition, previewCardBorderColor]"
  >
    <slot></slot>
  </div>
</template>

<script setup lang="ts">
const { defaultTransition, previewCardBorderColor } = useTailwindConfig()
</script>

<style scoped></style>
