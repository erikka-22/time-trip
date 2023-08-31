<script setup lang="ts">
const years = [
  {
    id:1,
    title:"~1899年",
    startYear: "1800",
    endYear: "1899",
    thumbnailUrl: "",
  },
  {
    id:2,
    title:"1900年代",
    startYear: "1900",
    endYear: "1909",
    thumbnailUrl: ""
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
    thumbnailUrl: ""
  },
  {
    id:5,
    title:"1930年代",
    startYear: "1930",
    endYear: "1939",
    thumbnailUrl: ""
  },
  {
    id:6,
    title:"1940年代",
    startYear: "1940",
    endYear: "1949",
    thumbnailUrl: ""
  },
  {
    id:7,
    title:"1950年代",
    startYear: "1950",
    endYear: "1959",
    thumbnailUrl: ""
  },
  {
    id:8,
    title:"1960年代",
    startYear: "1960",
    endYear: "1969",
    thumbnailUrl: ""
  },
  {
    id:9,
    title:"1970年代",
    startYear: "1970",
    endYear: "1979",
    thumbnailUrl: ""
  },
  {
    id:10,
    title:"1980年代",
    startYear: "1980",
    endYear: "1989",
    thumbnailUrl: ""
  },
  {
    id:11,
    title:"1990年代",
    startYear: "1990",
    endYear: "1999",
    thumbnailUrl: ""
  },
  {
    id:12,
    title:"2000年代",
    startYear: "2000",
    endYear: "2009",
    thumbnailUrl: ""
  },
  {
    id:13,
    title:"2010年代",
    startYear: "2010",
    endYear: "2019",
    thumbnailUrl: ""
  },
  {
    id:14,
    title:"2020年代",
    startYear: "2020",
    endYear: "2029",
    thumbnailUrl: ""
  },
]
</script>

<template>
  <YearItem v-for="(year, index) in years" 
    :key="year.id"
    :title="year.title"
    :start-year="year.startYear"
    :end-year="year.endYear"
    :thumbnail-url="year.thumbnailUrl"
    :id="year.id"
  />
</template>

