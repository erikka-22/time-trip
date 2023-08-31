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
  <v-card
    class="mx-auto"
    max-width="400"
    max-height="400"
  >
    <NuxtLink :to="{ 
      name: 'contents', 
      query: { 
        startYear: props.startYear, 
        endYear: props.endYear 
      } 
    }">
      {{ props.title }}
      <v-img :src="props.thumbnailUrl">
      </v-img>
    </NuxtLink>
  </v-card>
  
</template>