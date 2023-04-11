<template>
  <div style="height: 75vh">
      <!-- Start of Leaflet map -->
      <div id="map" style="height: 100vh">
          <client-only>
              <l-map :zoom=zoom :center=center :use-global-leaflet="false">
                  <l-tile-layer url="https://{s}.tile.osm.org/{z}/{x}/{y}.png"></l-tile-layer>
                  <l-marker :lat-lng="[17.4484363, 78.3741361]">
                      <l-popup ref="popup">
                          <div class="flex">
                              <img
                                  class="mt-3 h-10 w-10 rounded-full"
                                  src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
                                  width="500"
                                  height="600"
                              />
                              <div class="ml-2">
                                  <p>sdkgljsdhg</p>
                              </div>
                          </div>
                      </l-popup>
                  </l-marker>
              </l-map>
          </client-only>
      </div>
      <!-- End of Leaflet map-->
  </div>
</template>


<script setup lang="ts">
import { LMap, LTileLayer, LMarker, LPopup } from '@vue-leaflet/vue-leaflet'
// Leaflet css
import 'leaflet/dist/leaflet.css'
import { defineProps } from 'vue';
//using propps to get data
const props = defineProps({
  zoom: {
    type: Number,
    default:13
  },
  center:{
    type:Array,
    default:()=>[17.4484363, 78.3741361]

  },
  url:{

  },
  
});

</script>
