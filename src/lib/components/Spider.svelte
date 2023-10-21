<script lang="ts">
	import { Canvas } from '@threlte/core';
	import { T } from '@threlte/core';
	import { GLTF, OrbitControls } from '@threlte/extras';
</script>

<Canvas>
	<T.PerspectiveCamera makeDefault position={[10, 0, 10]} fov={20}>
		<OrbitControls enableDamping enableZoom={false} />
	</T.PerspectiveCamera>

	<T.AmbientLight />

	<T.DirectionalLight castShadow position={[5, 5, 5]} />

	<GLTF url="/assets/spider.glb" />
</Canvas>
