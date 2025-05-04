<script>
	import LabelHeading from '../utilities/LabelHeading.svelte';
</script>

<section class="partners-section section-padding">
	<LabelHeading title="Our Partners" color="#333)" />
	<!-- <p class="partners-description">
		We are proud to partner with organizations that share our vision of empowering ,supporting and
		uplifting women.
	</p> -->

	<div class="partners-container">
		<div class="partners-card">
			<img src="../asserts/partner1.png" alt="Partner 1" class="partners-card__image" />
		</div>
		<div class="partners-card">
			<img src="../asserts/partner2.png" alt="Partner 2" class="partners-card__image" />
		</div>
		<div class="partners-card">
			<img src="../asserts/partner3.png" alt="Partner 3" class="partners-card__image" />
		</div>
		<div class="partners-card">
			<img src="../asserts/partner4.png" alt="Partner 4" class="partners-card__image" />
		</div>
	</div>
</section>

<style>
	/* .partners-description {
		text-align: center;
		margin-bottom: 1rem;
	}

	.partners-title {
		font-size: 1rem;
		text-transform: uppercase;
	} */

	/* .partners-description {
		font-size: 0.9rem;
	} */

	.partners-container {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 2rem;
		margin: 2rem 0;

		background-color: var(--primary-color-opacity);
		padding: 2.5rem;
		border-radius: 0.5rem;
	}

	.partners-card {
		justify-self: center;
	}

	@media (min-width: 768px) {
		/* .partners-title {
			font-size: 2.4rem;
		}
		.partners-description {
			font-size: 1.2rem;
		} */

		.partners-card {
			width: 100%;
			max-width: 200px;
		}
	}

	@media (min-width: 1024px) {
		/* .partners-title {
			font-size: 3rem;
		}
		.partners-description {
			font-size: 1.5rem;
		} */
		.partners-card {
			width: 200px;
			max-width: 200px;
		}
	}

	@media (min-width: 1280px) {
		/* .partners-title {
			font-size: 3rem;
		}
		.partners-description {
			font-size: 1.5rem;
		} */
		.partners-card {
			width: 250px;
			max-width: 250px;
		}
	}
</style>
