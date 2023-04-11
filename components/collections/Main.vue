<template>
  <div>
    <ClientOnly>
      <!-- maps imported here -->
      <CollectionsMaps
        :url="url"
        :zoom="zoom"
        :center="center"
        :latlng="markerLatLng"
    /></ClientOnly>
  </div>
</template>
<script setup lang="ts">
const url = ref("https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png");

const zoom = ref(15);
const center = ref([51.505, -0.159]);
const markerLatLng = ref([51.504, -0.159]);
</script>
