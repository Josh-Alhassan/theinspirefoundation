<script>
	import DonateButton from '../utilities/DonateButton.svelte';
</script>

<section class="community-section section-padding">
	<div class="community-container">
		<h2 class="community-heading">Come Join us</h2>
		<p class="community-description">
			We need to reshape our own perception of how we view ourselves. We have to step up as women
			and take the lead
		</p>

		<DonateButton text="Join our Community" />
	</div>
</section>

<style>
	.community-section {
		background:
			linear-gradient(to right, rgba(0, 0, 0, 0.9), rgba(0, 0, 0, 0.7)),
			url('../asserts/community-img.jpg') no-repeat center center/cover;
		height: 500px;

		color: var(--text-color);
	}

	.community-heading {
		text-transform: uppercase;
		font-size: 0.8rem;
		border-bottom: 2px solid var(--text-color);
		padding-bottom: 1.5rem;
	}

	.community-description {
		margin: 2rem 0 3rem 0;
		font-size: 1.1rem;
		text-align: justify;
	}

	@media (min-width: 768px) {
		.community-section {
			height: 600px;
		}
		.community-heading {
			font-size: 1rem;
		}
		.community-description {
			font-size: 1.2rem;
		}
	}

	@media (min-width: 1024px) {
		.community-section {
			height: 700px;
		}
		.community-heading {
			font-size: 1.2rem;
		}
		.community-description {
			font-size: 1.5rem;
		}

		.community-container {
			max-width: 600px;
			margin: 0 auto;
		}
	}

	/* @media (min-width: 1280px) {
		.community-section {
			height: 800px;
		}
		.community-heading {
			font-size: 1.5rem;
		}
		.community-description {
			font-size: 1.8rem;
		}
	} */

	@media (min-width: 1920px) {
		.community-container {
			max-width: 1000px;
			margin: 0 auto;
		}
	}
</style>
