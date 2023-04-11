<template>
  <div>
    <ClientOnly>
        <!-- maps imported here -->
      <CollectionsMaps
        :url="url"
        :zoom="zoom"
        :center="center"
        :markerLating="markerLatLng"
        :attribution="attribution"
    /></ClientOnly>
  </div>
</template>
<script setup lang="ts">
const url = ref("https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png");
const attribution = ref(
  '&copy; <a target="_blank" href="http://osm.org/copyright">OpenStreetMap</a> contributors'
);
const zoom = ref(15);
const center = ref([51.505, -0.159]);
const markerLatLng = ref([51.504, -0.159]);
</script>
