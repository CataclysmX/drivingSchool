<template lang="html">
  <div class="h-full">
    <client-only>
      <l-map :zoom="13" :center="[45.3934, 4.2717]">
        <l-tile-layer url="http://{s}.tile.osm.org/{z}/{x}/{y}.png" />
        <l-marker :lat-lng="[45.38981, 4.26674]" class="grayscale-0" />
        <l-marker :lat-lng="[45.40395, 4.36657]" class="grayscale-0" />
        <l-marker :lat-lng="[45.4034521, 4.1837728]" class="grayscale-0" data-test="123456789" @click="log" />
      </l-map>
    </client-only>
  </div>
</template>

<script>
export default {
  name: 'LeafletMap',
  methods: {
    log (event, a) {
      console.log(a, this, event)
    }
  }
}
</script>

<style lang="css" scoped>
</style>
