<script setup lang="ts">
import THREE from 'three'
import { TresCanvas, useRenderLoop } from '@tresjs/core'
import { OrbitControls, GLTFModel } from '@tresjs/cientos'
import { shallowRef } from 'vue'

const astronautRef = shallowRef<THREE.Mesh>()
const { onLoop } = useRenderLoop()

const spaceman = '/src/assets/spaceman.glb'

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
            path="https://sketchfab-prod-media.s3.amazonaws.com/archives/d78d834779be41c5b62fa6f03dee3398/glb/117e8dc653ef42a287e20fcd7b96bd69/spaceman.glb?AWSAccessKeyId=ASIAZ4EAQ242OK362AHG&Signature=j3QmxKMUX%2FBrDbh8WANp7%2BGwWq8%3D&x-amz-security-token=IQoJb3JpZ2luX2VjEH4aCWV1LXdlc3QtMSJIMEYCIQCG8qB6mSWdNZP3tePPVPdwT1ri46lQD1nTChNG0jSMigIhAM02dT%2BcQhLts5WT5h%2FAZJS3ZPiiA2qtN2%2BaqsCE5tcLKrIFCEcQABoMNjc4ODc0MzcxODkyIgzaUysxeZfHRMvBbaYqjwVK1M3Wiw3LCOnWfuuOWKFQDopvQlMxGL8%2F8IPCatNdjMifFLyA7uZqIyA6%2FbcJYLodv5hNjm7LECSeZ1bxe0CBvuLxuwIJ4Qof49jZfey99TgvDR4PaNjVpEgg2vHJd9ltoV2NfGQL8JfloTAnpddVr%2BuViN%2Fly4i4basaHphvbk%2B4hLnWjPFCsQGm1Tp2KnKsYRIJLuB5BDOHpTh6%2FrRave87213NCnyW%2FbQBgHaxTZ%2BcIMMFdZ1va1yX%2BDT7TzZ1f3Fgt6M7ihkG2%2FnDd%2FjpFv6epBMRk%2BIkcjbM7RHIet0ZdC%2FkZv1g8H7Z7l2yL6YFoEof%2F3M%2Fj%2Bb9Nzo91bO7gb4%2F%2Ba4mAD64PnzfjRdl8SohpxNM6cBiU4QSsJ32bfIAEPeCxfmsKKmYhhX2P8aLlc%2BRHklHwlkmSv7DWMMqDCslPlJnFkJx64hKkQIdLVErxrw4Ss%2Bp699A2yIOLCFz%2F9ZCSDAV1MdK4v3ZziQdd1Wduh9xnmZNL32NGSB%2BD44VWviFY6vsn%2FdNmLTAHZVU8CZHlA0qlFnoyAeYbk%2F91EAj6wAoQDK4js4hghPuM9gdQ231K%2FrA1bUkH9zAdJq3o8eOtRLNmbqJ%2BS0Z%2FnifNa%2BFnc87QlmmTLtiDjZ13AQV4HKXXpx12nXczv8uan6%2FFe1n9TJ3asWzVq99%2FXHYlL0YFWxEI6jeePLfecold4cYoaDEZMctar1Fp%2BKxDuPFXC0StsZEL%2BNSVNxhADQBs%2B36ughQzi9m2vA1e8A2i90ZC0KsRQz2jGUxe9xllxeoH9NkyqtiLMnNEMQ8tfDTxgdyfxxGHw9%2Bn06hkJKiWT3rAWcXFrMC5c5UaKzSuslKUjhbpU5nCmx4w1IoHgFWMLWmurQGOrABfKNQx7RYgem23ZTl4TFn3gT%2BbwIGtbi28XVesYhZZfFvLwnppX6WUnUto%2FW01WjIq8zMQfby%2Bh1h8VuGug97rm9rUao29MBZDEPLhiaSRtp%2B5qowEigx3f%2FFLNf3nLR8t9x52HzQhb3zAuY%2BzTOwz%2F7YEnF61RnlFetW59j57%2B9sFRUasyehay0av9fNyYCkJXGdsKVwyR%2FX2LUag4rqOOW1rhMJMaYdX%2F4iJBl9PkA%3D&Expires=1720621040"
          />
        </TresMesh>
      </Suspense>
      <TresDirectionalLight :intensity="5" :position="[-1, 2.5, -1]" />
      <TresAmbientLight :intensity="1" />
    </TresCanvas>
  </div>
</template>
