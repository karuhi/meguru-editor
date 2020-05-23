<template>
  <div class="layout" :width="WindowWidth" :height="WindowHeight">
    <ZIllustration
      :width="WindowWidth"
      :height="WindowHeight"
      :props="{ dragRotate: true, resize: 'fullscreen' }"
    >
      <!-- 前面 -->
      <ZRect :stroke="10" :width="180" :height="180" color="red" :translate="{ x: 40, y: 40 }" />
      <ZRect :stroke="10" :width="100" :height="100" color="red" :translate="{ x: 40, y: 40 }" />
      <!-- 左面 -->
      <ZRect
        :stroke="10"
        :width="180"
        :height="180"
        color="blue"
        :translate="{ x: -40, y: 40 }"
        :rotate="{ y: TAU / 4 }"
      />
      <ZRect
        :stroke="10"
        :width="100"
        :height="100"
        color="blue"
        :translate="{ x: -40, y: 40 }"
        :rotate="{ y: TAU / 4 }"
      />
      <!-- 右面 -->
      <ZRect
        :stroke="10"
        :width="180"
        :height="180"
        color="green"
        :translate="{ x: 120, y: 40 }"
        :rotate="{ y: -TAU / 4 }"
      />
      <ZRect
        :stroke="10"
        :width="100"
        :height="100"
        color="green"
        :translate="{ x: 120, y: 40 }"
        :rotate="{ y: -TAU / 4 }"
      />
    </ZIllustration>
  </div>
</template>

<script>
import Zdog from 'zdog'
import { ZIllustration, ZRect, ZPolygon, ZAnchor } from 'vue-zdog'

export default {
  components: {
    ZIllustration,
    ZRect,
    ZPolygon,
    Zdog
  },
  data() {
    return {
      WindowWidth: window.innerWidth,
      WindowHeight: window.innerHeight,
      TAU: Zdog.TAU
    }
  }
}
</script>
<style scoped>
.zdog-canvas {
  width: 100%;
  height: 100%;
}
</style>
