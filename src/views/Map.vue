<template>
  <div class="map-page">
    <div class="map-page__title">Павелецкая</div>
    <google-map/>
    <div class="map-page__text">
      <p>Павелецкая — станция Замоскворецкой линии Московского метрополитена.
        Расположена между станциями Новокузнецкая и Автозаводская.
        Находится на территории района Замоскворечье</p>
    </div>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'
import GoogleMap from '../components/GoogleMap.vue'
export default Vue.extend({
  components: {
    GoogleMap
  }
})
</script>
<style lang="scss">
  .map-page {
    display: flex;
    flex-flow: column wrap;
    font-family: 'Lato', Arial, Helvetica, sans-serif;
    text-decoration: none;
    color: #000000bd;
    font-size: 25px;
    letter-spacing: 1px;

    &__title {
      font-weight: 300;
      letter-spacing: 2px;
      font-size: 30px;
      color: #000000bd;
      margin-bottom: 30px;
    }
  }
  .map {
    display: flex;
  }
</style>
