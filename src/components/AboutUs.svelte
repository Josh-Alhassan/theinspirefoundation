<script>
	import DonateButton from '../utilities/DonateButton.svelte';
	import Heading from '../utilities/Heading.svelte';
</script>

<section class="about-us section-padding">
	<!-- <h2 class="secondary-heading">About Us</h2> -->
	<Heading text="About Us" />
	<h3 class="about-us-tertairy-heading">
		Helping women never doubt that they are <span class="about-us-tertairy-heading-span">
			valuable & Powerful</span
		>
	</h3>

	<p class="about-us-description">
		Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic voluptas beatae ratione, porro quo
		corporis ullam earum fugit impedit neque deleniti minima quas, ipsa eveniet harum, eaque aperiam
		asperiores facilis.
	</p>

	<DonateButton href="/read-more" text="Read More" ariaLabel="Contribute to our cause" />
</section>

<style>
	.about-us-tertairy-heading {
		font-size: 1.5rem;
		line-height: 1.1;
		color: var(--text-color-dark);
		font-weight: 400;
		margin-bottom: 1.5rem;
	}

	.about-us-tertairy-heading-span {
		text-decoration: underline;
		font-weight: 600;
	}

	.about-us-description {
		font-size: 1rem;
		text-align: justify;
		margin-bottom: 2rem;
	}
</style>
