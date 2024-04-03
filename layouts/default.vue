<script setup lang="ts">
  const darkMode = ref(false)
</script>

<template>
  <div :class="{ dark: darkMode }">
    <div class="bg-white dark:bg-dim-900">
      <div class="min-h-full">
        <!-- TODO: Import left and right sidebars -->
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>