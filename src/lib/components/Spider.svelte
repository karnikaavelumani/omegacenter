<script lang="ts">
  import { T } from '@threlte/core'
  import { Environment, GLTF, OrbitControls } from '@threlte/extras'
</script>

<T.PerspectiveCamera
  makeDefault
  position={[10, 10, 10]}
  fov={25}
>
  <OrbitControls
    autoRotate
    enableDamping
  />
</T.PerspectiveCamera>

<T.AmbientLight />

<GLTF url="/assets/test.glb" />
