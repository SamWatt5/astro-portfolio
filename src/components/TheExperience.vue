<script lang="ts">
import { TresCanvas } from '@tresjs/core'
//import { TresPerspectiveCamera } from '@tresjs/core'
import { BasicShadowMap, SRGBColorSpace, NoToneMapping } from 'three'

const gl = {
    clearColor: '#181C3E',
    shadows: true,
    alpha: false,
    shadowMapType: BasicShadowMap,
    outputColorSpace: SRGBColorSpace,
    toneMappong: NoToneMapping,
}
</script>
<template>
    <div class="tres-container">
        <TresCanvas v-bind="gl" id="app">
            <TresPerspectiveCamera :position="[0, 0, 5]" />
            <TresMesh>
                <TresSphereGeometry :args="[1, 32, 32]" />
                <TresMeshNormalMaterial />
            </TresMesh>
        </TresCanvas>
    </div>
</template>

<style>
.tres-container {
    width: 100%;
    height: 400px;
}

#app{
    width: 100%;
    height:100%;
    background-color: red;
}
</style>