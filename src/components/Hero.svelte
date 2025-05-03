<script>
	import DonateButton from '../utilities/DonateButton.svelte';
	import Navigation from '../utilities/Navigation.svelte';

	export const backgroundImage = '../assets/hero-img.jpg';
	export const overlayOpacity = 0.7;
	export const statsText = '100+ projects within Nigeria';
	export const title = 'Women in Action';
	export const description =
		'We work towards ensuring a life free from inequality and discrimination for every woman';
</script>

<header class="hero-section" aria-label="Hero section">
	<Navigation />

	<div class="jumbotron">
		{#if statsText}
			<span class="span-heading">{statsText}</span>
		{/if}
		<h1 class="primary-heading">{title}</h1>

		{#if description}
			<p class="heading-description">
				{description}
			</p>
		{/if}
		<DonateButton />
	</div>
</header>

<style>
	.hero-section {
		background:
			linear-gradient(to right, rgba(0, 0, 0, 0.9), rgba(0, 0, 0, 0.7)),
			url('../asserts/hero-img.jpg') no-repeat top center/cover;
		height: 60vh;
	}

	.jumbotron {
		height: 100%;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;

		color: var(--text-color);

		text-align: center;

		padding: 0 0.5rem;
	}

	.span-heading {
		font-size: 0.8rem;
	}
	.primary-heading {
		font-size: 2rem;
	}

	.heading-description {
		font-size: 1rem;
		margin-bottom: 1.5rem;
	}

	@media (min-width: 425px) {
		.jumbotron {
			padding: 0 2rem;
		}

		.heading-description {
			margin-bottom: 1.3rem;
		}
	}

	@media (min-width: 768px) {
		.jumbotron {
			padding: 0 6rem;
		}

		.span-heading {
			font-size: 1rem;
		}
		.primary-heading {
			font-size: 3rem;
			margin-bottom: 0.5rem;
		}

		.heading-description {
			font-size: 1.2rem;
			margin-bottom: 2rem;
		}
	}

	@media (min-width: 1024px) {
		.hero-section {
			height: 80vh;
		}
		.jumbotron {
			padding: 0 10rem;
			height: 90%;
		}

		.span-heading {
			font-size: 1.2rem;
		}

		.primary-heading {
			font-size: 3.5rem;
		}
		.heading-description {
			font-size: 1.5rem;
			margin-bottom: 2.5rem;

			width: 75%;
		}
	}

	@media (min-width: 1280px) {
		.jumbotron {
			padding: 0 15rem;
		}
		.primary-heading {
			font-size: 4rem;
		}

		.heading-description {
			font-size: 1.5rem;
			margin-bottom: 3rem;
		}
	}

	@media (min-width: 1920px) {
		.heading-description {
			width: 55%;
		}
		.jumbotron {
			max-width: 1920px;
			margin: 0 auto;
		}
	}
</style>
