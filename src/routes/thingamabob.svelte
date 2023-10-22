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
			'Check out our latest release reaching rave reviews from multiple buyers. This intricate device is a captivating blend of countless knobs, buttons, mesmerizing lights, and so much more. Grab one today before they are all sold out!',
		price: 99.99,
		stars: 4.5,
		maxStars: 5,
		features: ['QuantumLink TactiPulse Actuators', 'NanoTactiKey Electro-Fusion Keypad', 'LuminaFusion SmartGlow IllumiNode']
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
				<h3>{data.title}</h3>
			</div>
			<div class="thingamabob-rating">
				<p>{formattedStars} {data.stars}/{data.maxStars} stars</p>
			</div>
			<div class="thingamabob-description">
				<p>{data.description}</p>
			</div>
			<div class="thingamabob-features">
				<h3>Features</h3>
				<ul>
					{#each data.features as feature}
						<li>{feature}</li>
					{/each}
				</ul>
			</div>
			<div class="thingamabob-price">
				<h3>Price</h3>
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
		justify-self: center;
		align-self: center;
		grid-template-columns: 1fr 1fr;
		margin: 0 10em 0 10em;
	}

	.thingamabob-image {
		display: flex;
		justify-content: center;
		align-items: center;
		
		max-height: 100vh;
		max-width: 50vw;
	}

	.thingamabob-text {
		padding: 20px;
	}

	.thingamabob-header,
	.thingamabob-features,
	.thingamabob-price {
		font-weight: 500;
	}

	.thingamabob-rating {
		font-weight: 600;
	}

	.thingamabob-description {
		font-size: 12px;
	}

	.thingamabob-features ul {
		font-size: 12px;
		font-weight: 300;
	}

	@media (max-width: 1020px) {
		.thingamabob-content {
			grid-template-columns: 1fr;
			margin: 0;
		}

		.thingamabob-image {
			max-height: 50vh;
			max-width: 100vw;
		}
	}
</style>
