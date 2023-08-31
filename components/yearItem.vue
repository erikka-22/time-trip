<script setup lang="ts">
const props = defineProps<{
  id: number
  title: string
  startYear: string,
  endYear: string,
  thumbnailUrl: string
}>()

// const get
</script>
<template>
  <NuxtLink :to="{ 
    name: 'contents', 
    query: { 
      startYear: props.startYear, 
      endYear: props.endYear 
    } 
  }">
    {{ props.title }}
  </NuxtLink>
  <img :src="props.thumbnailUrl">
</template>