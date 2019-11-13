<template>
  <section class="container">
    <div v-if="isMounted">
      <yandex-map
        :coords="[43.24817754432621, 76.93266032039878]"
        zoom="13"
      >

    <ymap-marker
      marker-type="placemark"
      :coords="[43.26410799233756, 76.92987082302332]"
      :balloon="{body: 'Мега парк'}"
      :iconContent="{body: 'Мега парк'}"
      cluster-name="1"
    ></ymap-marker>

    <ymap-marker
      marker-type="placemark"
      :coords="[43.23053604152807, 76.945977]"
      cluster-name="1"
      hintContent='Нурлы-тау'
      :icon="options"
    ></ymap-marker>
</yandex-map>
    </div>
  </section>
</template>

<script>
/* eslint-disable */
import YmapPlugin from 'vue-yandex-maps'
import Vue from 'vue'
export default {
  data(){
    return{
      isMounted: false,
      options: {
        layout: "default#image",
        imageHref: "/img/zakladka.png",
        imageSize: [40, 80],
        imageOffset: [-20, -20],
        contentOffset: [0, 0]
      }
    }
  },
  mounted () {
    // register globally
    Vue.use(YmapPlugin)
    this.isMounted = true
  }
}
</script>

<style>
.ymap-container {
  height: 600px;
}
</style>
