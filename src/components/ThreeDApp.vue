<script lang="ts">
import { TresCanvas } from '@tresjs/core'
import { BasicShadowMap, SRGBColorSpace, NoToneMapping } from 'three'

const gl = {
  clearColor: '#181C3E',
  shadows: true,
  alpha: false,
  shadowMapType: BasicShadowMap,
  outputColorSpace: SRGBColorSpace,
  toneMapping: NoToneMapping,
}
</script>

<template>
    <div class="tres-container">
        <TresCanvas v-bind="gl">
            <TresPerspectiveCamera :position="[0, 0, 5]" />
        </TresCanvas>
    </div>
</template>

<style>
    .tres-container {
      width: 100%;
      height: 400px;
    }
</style>