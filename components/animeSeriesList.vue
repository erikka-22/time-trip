<script setup lang="ts">
const route = useRoute()

const { data: animeSeriesResponse } = await useFetch(`https://mediag.bunka.go.jp/sparql/?query=PREFIX%20rdf%3A%20%3Chttp%3A%2F%2Fwww.w3.org%2F1999%2F02%2F22-rdf-syntax-ns%23%3E%0APREFIX%20rdfs%3A%20%3Chttp%3A%2F%2Fwww.w3.org%2F2000%2F01%2Frdf-schema%23%3E%0APREFIX%20ma%3A%20%3Chttps%3A%2F%2Fmediaarts-db.bunka.go.jp%2Fdata%2Fproperty%23%3E%20%0APREFIX%20schema%3A%20%3Chttps%3A%2F%2Fschema.org%2F%3E%0APREFIX%20maid%3A%20%3Chttps%3A%2F%2Fmediaarts-db.bunka.go.jp%2Fid%2F%3E%0ASELECT%20%3Fitem%20%3FitemLabel%20%3Fgenre%20%3Fyear%20%3FendYear%20WHERE%20%7B%0A%20%09%3Fitem%20schema%3Agenre%20%3Fgenre%3B%0A%20%20%20%20%09%09%09%20%20rdfs%3Alabel%20%3FitemLabel%3B%0A%20%20%20%20%20%20%20%20%20%09%09schema%3AdatePublished%20%3Fdate%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20schema%3AendDate%20%24endDate%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20BIND%20(SUBSTR(%3Fdate%2C%201%2C%204)%20AS%20%3Fyear)%0A%20%20%09%09%09%09%09BIND%20(SUBSTR(%3FendDate%2C%201%2C%204)%20AS%20%3FendYear)%0A%20%20%09%09%09%09%09FILTER%20((%3Fyear%20%3C%3D%20%22${route.query.endYear}%22)%20%26%26%20(%3FendYear%20%3E%3D%20%22${route.query.startYear}%22))%0A%20%20%09%09%09%09%09FILTER%20(%3Fgenre%20%3D%20%22%E3%82%A2%E3%83%8B%E3%83%A1%E3%83%86%E3%83%AC%E3%83%93%E3%83%AC%E3%82%AE%E3%83%A5%E3%83%A9%E3%83%BC%E3%82%B7%E3%83%AA%E3%83%BC%E3%82%BA%22)%0A%7D%20order%20by%20asc(%3Fyear)%20&format=json`)
const contents = animeSeriesResponse.value.results.bindings
</script>

<template>
  <h2>アニメテレビレギュラーシリーズ</h2>
  <v-list>
    <contentItem v-for="(content, index) in contents" 
      :key="index"
      :title="content.itemLabel.value"
      :startYear="content.year.value"
      :endYear="content.endYear.value"
      :url="content.item.value"
    />
  </v-list>
  
</template>