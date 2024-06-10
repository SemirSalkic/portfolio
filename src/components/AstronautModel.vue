<script setup lang="ts">
import THREE from 'three'
import { TresCanvas, useRenderLoop } from '@tresjs/core'
import { OrbitControls, GLTFModel } from '@tresjs/cientos'
import { shallowRef } from 'vue'

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
          <GLTFModel
            path="https://sketchfab-prod-media.s3.amazonaws.com/archives/d78d834779be41c5b62fa6f03dee3398/glb/117e8dc653ef42a287e20fcd7b96bd69/spaceman.glb?AWSAccessKeyId=ASIAZ4EAQ242ECCQY75X&Signature=Lp%2Bo67fQWipfzw7F%2Byfxpur7Gns%3D&x-amz-security-token=IQoJb3JpZ2luX2VjEJv%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCWV1LXdlc3QtMSJIMEYCIQDvCcOf677oEoX%2BKx5ICh6nyQA5LAUosKx4X901J25wNgIhAIdJvlzMtzLphZwvjpKqIXnYMLZmw0N3JAILcuF65ibxKrEFCDMQABoMNjc4ODc0MzcxODkyIgw%2BryBQ8xEdbcVyXjMqjgVeXbMckVtVbVWODj5IdBLytquMEYEZqD04b3izz8pufoZ8V7Fz3H3%2BLTJ5%2FmaLRa2moTfpLVNHFs6%2FrWx2bCrTAzMPFg5L9V5d%2BGulO4J6L2U42Bmqte3ddr5ulh00sdTvjtUn8sX%2BqiYK6NMOsPa3pGvaDf%2FhpB0%2FHBskGudytIBCeTD7CvQjjncqsFi6dh3f6oAFxPBBVIw6sXu0pfuvwHSI1Y9Ajevx0DUdx3No7vhkX30HKrf8Yq5T2L6zGdhrBEgmNX62%2BbERMZpvLKa0pqnImbU%2FO7Ro9F528PmhQf8APsE5Dd%2FQ79cTSswAYEbqhklN8R3r8%2Bs0hWiUuISpoI%2FfoOEeaiGkn9mwAkx02VvhK%2FCJwuA90OZ6hKf6n%2FdDYZOERFx6ur6y0UCIg0lpA6QhpHjizZ0gtHtoDZv76mt2zEoeCWocMFIn9YbIXCk7VDgEaR3LEG1rD%2Btl6YF4d%2FPuYRttTA9YZlE0wHLo%2B4lRei3GP2bQpkmY6xDXaqMv%2BbFykyqa3%2FVm7PcI8m3nifYVL47aG5rYAs576wxp4JKAeahF1YeBC76yb3ASsey1PcKauhZX0fUAXTrafrW01hfQclugT%2Bk%2B4N1kW6yCy6Wrqlu9jkHXtK2EAMM4BnWmgdauvvg0VDI0Myhg3V5BXV3ODFt2M31nL9yQRk26nfX51THJdqkVx%2FgKMtcH%2FmQ4e3e%2FNFGeArZiVykVyWFI4Ln4oAcqwvI1m%2Bizb4R0Sgq%2BzE%2FFyRwYXYsJJmzUkd8w4r%2FsT7NDKHOiEW4XhDZQ1TbmT8WErhFM3Usw4%2FY2vipAigzvXNtEIo871pkHiKqhVyIIwkonxmFqYog4GtBPok8gcKl6GkwIsk%2Bxk3IwlOOXswY6sAEyi1wgrhveHzl%2FmHZjAKl8tyU9SX%2FS32IeGKUiWqlz5ep%2B5sIaTxt3FftVcICXkt2pnBoSoaVU%2Bkgz1gr3Fa5xxy3JIR95qhsaW1nT6Nsto4ZpPLRyBsDX8pK%2BkJP6a4%2FmbygYNhgnS6I3NGoP5ef6ujYwW6Ons3eKZTcCmh40bbGCKYKhneFiLZx3ky5bJ0HMtTlDa0xfZq4n94icIWaonahutA8GgorePGPQ%2BQ22Hw%3D%3D&Expires=1717958963"
          />
        </TresMesh>
      </Suspense>
      <TresDirectionalLight :intensity="5" :position="[-1, 2.5, -1]" />
      <TresAmbientLight :intensity="1" />
    </TresCanvas>
  </div>
</template>
