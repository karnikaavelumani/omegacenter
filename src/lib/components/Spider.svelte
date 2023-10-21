<script lang="ts">
  import { T } from '@threlte/core'
  import { Environment, GLTF, OrbitControls } from '@threlte/extras'
</script>

<T.PerspectiveCamera
  makeDefault
  position={[10, 0, 10]}
  fov={20}
>
  <OrbitControls
    enableDamping
    enableZoom={false}
  />
</T.PerspectiveCamera>

<T.AmbientLight />

<T.DirectionalLight
  castShadow
  position={[5, 5, 5]}
/>

<GLTF url="/assets/spider.glb" />
