<script setup lang="ts">
import { TresCanvas } from '@tresjs/core'


</script>

<template>
  <TresCanvas
    clear-color="#82DBC5"
    window-size
  >
    <TresPerspectiveCamera
      :position="[3, 3, 3]"
      :look-at="[0, 0, 0]"
    />

    <TresMesh :position="[0,0,0]">
      <TresTorusGeometry :args="[1, 0.5, 16, 32]" />
      <TresMeshBasicMaterial color="orange" />
    </TresMesh>

    <TresMesh :position="[0, 0, 2]" :scale="[3, 1, 1]" :rotation="[0, 0, 0]">
      <TresBoxGeometry :args="[1, 1, 1]" />
      <TresMeshBasicMaterial color="green" />
    </TresMesh>

    <TresAxesHelper/>
    <TresAmbientLight :intensity="1" />
  </TresCanvas>
</template>

<style>
html,
body {
  margin: 0;
  padding: 0;
  height: 100%;
  width: 100%;
}
#app {
  height: 100%;
  width: 100%;
}
</style>