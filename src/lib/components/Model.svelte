<script lang="ts">
	import { Canvas } from '@threlte/core';
	import { T } from '@threlte/core';
	import { GLTF, OrbitControls } from '@threlte/extras';
</script>

<Canvas>
	<T.PerspectiveCamera makeDefault position={[10, 5, 10]} fov={40}>
		<OrbitControls enableDamping autoRotate enableZoom={false} />
	</T.PerspectiveCamera>

	<T.AmbientLight />

	<T.DirectionalLight castShadow intensity={3} position={[8, 5, 0]} />

	<GLTF url="/assets/thingamabob.glb"/>
	
	<!-- <T.Mesh position={[0, -3, 0]} rotation.x={-Math.PI/2} receiveShadow>
		<T.CircleGeometry args={[10, 40]}/>
		<T.MeshStandardMaterial color="blue" />
	</T.Mesh> -->
</Canvas>
