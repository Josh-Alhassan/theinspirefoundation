<script>
	import DonateButton from '../utilities/DonateButton.svelte';
	import Heading from '../utilities/Heading.svelte';
	import TertiaryHeading from '../utilities/TertiaryHeading.svelte';
	import ImpactProjects from './ImpactProjects.svelte';
</script>

<section class="about-us section-padding">
	<!-- <h2 class="secondary-heading">About Us</h2> -->
	<Heading text="About Us" />
	<TertiaryHeading
		text="Helping women never doubt that they are"
		highlightedText="Valuable & Powerful"
	/>

	<p class="about-us-description">
		Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic voluptas beatae ratione, porro quo
		corporis ullam earum fugit impedit neque deleniti minima quas, ipsa eveniet harum, eaque aperiam
		asperiores facilis.
	</p>

	<DonateButton href="/read-more" text="Read More" ariaLabel="Contribute to our cause" />

	<ImpactProjects />
</section>

<style>
	.about-us-description {
		font-size: 1rem;
		text-align: justify;
		margin-bottom: 2rem;
	}

	@media (min-width: 768px) {
		.about-us-description {
			font-size: 1.2rem;
		}
	}

	@media (min-width: 1024px) {
		.about-us-description {
			font-size: 1.5rem;
		}
	}

	@media (min-width: 1920px) {
		.about-us {
			max-width: 1920px;
			margin: 0 auto;
		}
	}
</style>
