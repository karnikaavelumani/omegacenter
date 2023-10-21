<script lang="ts">
	export let data: {
		title: string;
		description: string;
		price: number;
		stars: number;
		maxStars: number;
		features: string[];
	} = {
		title: 'Thingamabob',
		description:
			'Check out our latest release reaching rave reviews from many buyers. This intricate device is a captivating blend of countless knobs, buttons, mesmerizing lights, and so much more. Grab one today before they are all sold out!',
		price: 99.99,
		stars: 4.5,
		maxStars: 5,
		features: ['Knobs', 'Buttons', 'Lights', 'More']
	};

	const formattedStars = Array.from({ length: data.maxStars }, (_, i) =>
		i < Math.floor(data.stars) ? '⭐' : '✩'
	).join('');
</script>

<section class="thingamabob-container">
	<div class="thingamabob-content">
		<div class="thingamabob-image">
			<slot />
		</div>
		<div class="thingamabob-text">
			<div class="thingamabob-header">
				<h1>{data.title}</h1>
			</div>
			<div class="thingamabob-rating">
				<p>{formattedStars} {data.stars}/{data.maxStars} stars</p>
			</div>
			<div class="thingamabob-description">
				<p>{data.description}</p>
			</div>
			<div class="thingamabob-features">
				<h2>Features</h2>
				<ul>
					{#each data.features as feature}
						<li>{feature}</li>
					{/each}
				</ul>
			</div>
			<div class="thingamabob-price">
				<h2>Price</h2>
				<p>
					{data.price.toLocaleString('en-US', {
						style: 'currency',
						currency: 'USD'
					})}
				</p>
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
			max-width: 80vw;
		}
	}
</style>
