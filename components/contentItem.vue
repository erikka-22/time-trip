<script setup lang="ts">
const props = defineProps<{
  title: string,
  startYear: string,
  endYear: string,
  url: string,
}>()

</script>

<template>
  <v-list-item>
    <p>{{ props.title }}</p>
    <p>{{ props.startYear }}</p>
    <p>{{ props.endYear }}</p>
  </v-list-item>

</template>