<script setup lang="ts">
const route = useRoute()
const year = route.query.startYear
</script>

<template>
  <h1>{{ year }}年代のメディア芸術</h1>
  <v-list lines="one">
    <MangaMagazineList />
    <MangaSeriesList />
    <AnimeSeriesList />
  </v-list>
</template>