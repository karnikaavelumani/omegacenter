<script lang="ts">
	import App from '$lib/components/App.svelte';
</script>

<section class="thingamabob-container">
	<div class="thingamabob-content">
		<div class="thingamabob-image">
			<App />
		</div>
		<div class="thingamabob-text">
			<div class="thingamabob-header">
				<h1>Thingamabob</h1>
			</div>
			<div class="thingamabob-rating">
				<p>⭐⭐⭐⭐✩ 4.5/5 stars</p>
			</div>
			<div class="thingamabob-description">
				<p>
					Check out our latest release reaching rave reviews from many buyers. This intricate device
					is a captivating blend of countless knobs, buttons, mesmerizing lights, and so much more.
					Grab one today before they are all sold out!
				</p>
			</div>
			<div class="thingamabob-features">
				<h2>Features</h2>
				<ul>
					<li>Knobs</li>
					<li>Buttons</li>
					<li>Lights</li>
					<li>More</li>
				</ul>
			</div>
			<div class="thingamabob-price">
				<h2>Price</h2>
				<p>$99.99</p>
			</div>
		</div>
	</div>
</section>

<style>
	.thingamabob-container {
		display: grid;
	}

	.thingamabob-content {
		display: grid;
		grid-template-columns: 2fr 1fr;
		margin: 0 5em 0 5em;
	}

	.thingamabob-image {
		display: flex;
		justify-content: center;
		align-items: center;
		min-height: 200px;
		max-height: 100vh;
		max-width: 50vw;
		border: 4px dashed grey;
	}

	.thingamabob-text {
		padding: 20px;
	}

	@media (max-width: 1020px) {
		.thingamabob-content {
			grid-template-columns: 1fr;
			margin: 0;
		}

		.thingamabob-image {
			max-width: 100vw;
		}
	}
</style>
