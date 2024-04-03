<template>
  <div
    class="m-2 border bg-gray-50 rounded-2xl overflow-hidden dark:bg-dim-700"
    :class="previewCardBorderColor"
  >
    <h3
      class="text-xl p-3 font-extrabold text-gray-900 border-b dark:text-white"
    >
      {{ props.title }}
    </h3>

    <slot></slot>

    <button
      :class="defaultTransition"
      class="w-full p-3 text-sm text-blue-400 cursor-pointer hover:bg-gray-100 dark:hover:bg-dim-300"
    >
      Show more
    </button>
  </div>
</template>

<script setup lang="ts">
const { previewCardBorderColor, defaultTransition } = useTailwindConfig();

const props = defineProps({
  title: {
    type: String,
    required: true,
  },
});
</script>

<style scoped></style>
