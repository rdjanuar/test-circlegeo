<template>
  <MglMap :data="data" :map-style="style" :center="center" :zoom="zoom" width="100vw" height="100vh">
    <MglNavigationControl />
    <MglGeoJsonSource source-id="geojson" :data="data">
      <MglCircleLayer
        layer-id="geojson"
        :paint="{
          'circle-color': 'red',
          'circle-opacity': 1,
          'circle-radius': 6,
        }"
      />
    </MglGeoJsonSource>
  </MglMap>
</template>

<script setup>
import { data } from "./data";

const style = "https://api.maptiler.com/maps/streets/style.json?key=cQX2iET1gmOW38bedbUh";
const center = [107.6689, -6.9175];
const zoom = 8;
</script>
