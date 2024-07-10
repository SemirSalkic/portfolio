<script setup lang="ts">
import THREE from 'three'
import { TresCanvas, useRenderLoop } from '@tresjs/core'
import { OrbitControls, GLTFModel } from '@tresjs/cientos'
import { shallowRef } from 'vue'
import spacemanScene from '../assets/spaceman.glb?url'

const astronautRef = shallowRef<THREE.Mesh>()
const { onLoop } = useRenderLoop()

onLoop(({ delta, elapsed }) => {
  if (!astronautRef.value) return

  // Slow down the movement
  // const slowElapsed = elapsed / 5

  // Animate using trigonometry
  astronautRef.value.position.y = Math.sin(elapsed) * 1.5
  // astronautRef.value.position.x = (1 - Math.cos(elapsed)) * 1.5

  // // Change direction when reaching the peak
  // if (astronautRef.value.position.y < 0) {
  //   astronautRef.value.position.y = 0
  // }
})
</script>

<template>
  <div class="min-h-screen">
    <TresCanvas>
      <TresPerspectiveCamera :fov="65" :position="[20, 3, -9]" />
      <OrbitControls :enable-zoom="false" />
      <Suspense>
        <TresMesh ref="astronautRef" :rotation="[6, 2.1, 6.5]">
          <GLTFModel :path="spacemanScene" />
        </TresMesh>
      </Suspense>
      <TresDirectionalLight :intensity="5" :position="[-1, 2.5, -1]" />
      <TresAmbientLight :intensity="1" />
    </TresCanvas>
  </div>
</template>
