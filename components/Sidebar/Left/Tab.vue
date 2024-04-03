<script setup lang="ts">

const props = defineProps({
  name: {
    type: String,
    required: false,
    default: ''
  },
  href: {
    type: String,
    required: true,
    default: '/'
  }
})

const route = useRoute()
const { defaultTransition } = useTailwindConfig()

const textClasses = computed(() => props.href === route.path ? 'font-bold' : 'font-semibold')
</script>

<template>
  <NuxtLink :to="props.href" :class="defaultTransition" class="flex items-center w-min p-3 hover:bg-gray-200 rounded-full dark:text-white dark:hover:bg-dim-200">
    <div class="w-8 h-8">
      <slot></slot>
    </div>

    <div class="ml-3 font-bold text-xl" :class="textClasses">
      <span>{{ props.name }}</span>
    </div>
  </NuxtLink>
</template>

<style scoped>

</style>