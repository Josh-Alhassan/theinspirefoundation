<script>
	import Heading from '../utilities/Heading.svelte';
	import MakeDonations from '../utilities/MakeDonations.svelte';
	import TertiaryHeading from '../utilities/TertiaryHeading.svelte';
</script>

<section class="events-section section-padding">
	<div class="events-container">
		<div>
			<Heading text="Events" />
			<TertiaryHeading text="We organize inclusive events for" highlightedText="Women & Girls" />
		</div>

		<MakeDonations />
	</div>
</section>

<style>
	@media (min-width: 1024px) {
		.events-container {
			display: flex;
			justify-content: space-between;
			align-items: center;
			gap: 5rem;
		}
	}

	@media (min-width: 1440px) {
		.events-container {
			gap: 7rem;
		}
	}
	@media (min-width: 1920px) {
		.events-container {
			max-width: 1920px;
			margin: 0 auto;

			justify-content: center;
		}
	}
</style>
