<script setup lang="ts">
const props = defineProps<{
  title: string,
  startYear: string,
  endYear: string,
  url: string,
}>()

</script>

<template>
  <v-card
    color="grey-lighten-5"
    :title="props.title"
    class="my-4"
  >
    <v-card-item class="py-1">開始:{{ props.startYear }}年</v-card-item>
    <v-card-item class="py-1">終了:{{ props.endYear }}年</v-card-item>
    <v-card-action>
      <v-btn :href="props.url">
        詳細を見る
      </v-btn>
    </v-card-action>  
  </v-card>

</template>