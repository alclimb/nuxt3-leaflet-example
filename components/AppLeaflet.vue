<script lang="ts" setup>
import L from "leaflet";
import "leaflet/dist/leaflet.css";

/** テンプレート参照: マップ表示用のDOM要素 */
const mapEl = ref<HTMLElement>();

// MEMO: テンプレート参照(mapEl)はonMounted内で使える
onMounted(() => {
  // leafletのセットアップ
  const map = L.map(mapEl.value).setView([37.9022418, 139.0235109], 13);

  // 地図情報を読み込み
  L.tileLayer(`https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png`, {
    maxZoom: 19,
    attribution: `© OpenStreetMap`,
  }).addTo(map);

  // マーカーピンの設定
  L.marker([37.9022418, 139.0235109], { opacity: 0.8 })
    .addTo(map)
    .bindPopup(`<b>Hello world!</b><br>I am a popup.`);
});
</script>

<template>
  <!-- 地図表示エリア -->
  <div ref="mapEl" style="width: 1024px; height: 768px"></div>
</template>
