<script setup lang="ts">
const years = [
  {
    id:1,
    title:"~1899年",
    startYear: "1800",
    endYear: "1899",
    thumbnailUrl: "https://www.lib.pref.saitama.jp/iipsrv/iipsrv.fcgi?IIIF=/1498300601/000000001.tif/full/500,/0/default.jpg",
  },
  {
    id:2,
    title:"1900年代",
    startYear: "1900",
    endYear: "1909",
    thumbnailUrl: "https://ibmuseum.mapps.ne.jp/files/9722/media_files/large/107927.jpg"
  },
  {
    id:3,
    title:"1910年代",
    startYear: "1910",
    endYear: "1919",
    thumbnailUrl: "https://ibmuseum.mapps.ne.jp/files/9722/media_files/large/919.jpg"
  },
  {
    id:4,
    title:"1920年代",
    startYear: "1920",
    endYear: "1929",
    thumbnailUrl: "https://www.lib.pref.saitama.jp/iipsrv/iipsrv.fcgi?IIIF=/1498300918/000000001.tif/full/500,/0/default.jpg"
  },
  {
    id:5,
    title:"1930年代",
    startYear: "1930",
    endYear: "1939",
    thumbnailUrl: "https://ibmuseum.mapps.ne.jp/files/9722/media_files/large/72506.jpg"
  },
  {
    id:6,
    title:"1940年代",
    startYear: "1940",
    endYear: "1949",
    thumbnailUrl: "https://ibmuseum.mapps.ne.jp/files/9722/media_files/large/48093.jpg"
  },
  {
    id:7,
    title:"1950年代",
    startYear: "1950",
    endYear: "1959",
    thumbnailUrl: "https://ibmuseum.mapps.ne.jp/files/8088/media_files/large/9762.jpg"
  },
  {
    id:8,
    title:"1960年代",
    startYear: "1960",
    endYear: "1969",
    thumbnailUrl: "https://ibmuseum.mapps.ne.jp/files/9722/media_files/large/86492.jpg"
  },
  {
    id:9,
    title:"1970年代",
    startYear: "1970",
    endYear: "1979",
    thumbnailUrl: "https://ibmuseum.mapps.ne.jp/files/8088/media_files/large/9615.jpg"
  },
  {
    id:10,
    title:"1980年代",
    startYear: "1980",
    endYear: "1989",
    thumbnailUrl: "https://ibmuseum.mapps.ne.jp/files/8088/media_files/large/9584.jpg"
  },
  {
    id:11,
    title:"1990年代",
    startYear: "1990",
    endYear: "1999",
    thumbnailUrl: "https://ibmuseum.mapps.ne.jp/files/9722/media_files/large/44213.jpg"
  },
  {
    id:12,
    title:"2000年代",
    startYear: "2000",
    endYear: "2009",
    thumbnailUrl: "https://ibmuseum.mapps.ne.jp/files/9722/media_files/large/7264.jpg"
  },
  {
    id:13,
    title:"2010年代",
    startYear: "2010",
    endYear: "2019",
    thumbnailUrl: "https://ibmuseum.mapps.ne.jp/files/9722/media_files/large/139191.jpg"
  },
  {
    id:14,
    title:"2020年代",
    startYear: "2020",
    endYear: "2029",
    thumbnailUrl: "https://ibmuseum.mapps.ne.jp/files/9722/media_files/large/205904.jpg"
  },
]
</script>

<template>
  <v-container>
    <v-row>
      <v-col>
      <YearItem v-for="year in years" 
        :key="year.id"
        :title="year.title"
        :start-year="year.startYear"
        :end-year="year.endYear"
        :thumbnail-url="year.thumbnailUrl"
        :id="year.id"
      />
      </v-col>
    </v-row>
  </v-container>
</template>

