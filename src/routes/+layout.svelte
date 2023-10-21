<script lang="ts">
	import Navbar from '$lib/components/nav/bar.svelte';
	import Footer from '$lib/components/footer/footer.svelte';
</script>

<Navbar />
<main><slot /></main>
<Footer />
