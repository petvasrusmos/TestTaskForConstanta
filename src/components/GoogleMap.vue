<template>
  <div>
    <GmapMap
      class="map"
      :center="{lat:55.731482, lng:37.636277}"
      :zoom="15"
    >
      <GmapMarker
        :position="{ lat:55.731482, lng:37.636277 }"
        clickable
        draggable
      />
    </GmapMap>
  </div>
</template>
<script lang>
import Vue from 'vue'
import * as VueGoogleMaps from 'vue2-google-maps'
// key: AIzaSyD9Gu9CqdvDTCoiMComaxXaGa24a0bSK_0
Vue.use(VueGoogleMaps, {
  load: {
    key: 'AIzaSyD9Gu9CqdvDTCoiMComaxXaGa24a0bSK_0',
    libraries: 'places'
  },
  installComponents: true
})
export default Vue.extend({
  name: 'GoogleMap',
  data () {
    return {
      options: {
        zoom: 10,
        center: {
          lat: 39.9995601,
          lng: -75.1395161
        },
        mapTypeId: 'roadmap'
      }
    }
  },
  // computed: {
  //   google: gmapApi
  // },
  methods: {
    myclick () {
      console.log(1111111111111111)
    }
  }
})
</script>
<style lang="scss">
  .map {
    display: flex;
    flex: 1 1 100%;
    width: 100%;
    height: 300px;
    z-index: 3;
  }
</style>
