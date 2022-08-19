<script lang="ts" setup>
import L from "leaflet";
import "leaflet/dist/leaflet.css";

const mapEl = ref<HTMLElement>();

onMounted(() => {
  //
  const map = L.map(mapEl.value).setView([37.9022418, 139.0235109], 13);

  L.tileLayer(`https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png`, {
    maxZoom: 19,
    attribution: `© OpenStreetMap`,
  }).addTo(map);

  const marker = L.marker([37.9022418, 139.0235109], { opacity: 0.8 }).addTo(
    map
  );

  marker.bindPopup(`<b>Hello world!</b><br>I am a popup.`);
});
</script>

<template>
  <div ref="mapEl" style="width: 1024px; height: 768px"></div>
</template>
