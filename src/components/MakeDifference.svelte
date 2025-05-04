<script>
	import DonateButton from '../utilities/DonateButton.svelte';
	import LabelHeading from '../utilities/LabelHeading.svelte';
</script>

<section class="humaniterian-section section-padding">
	<LabelHeading title="Want to make a difference?" color="#fff" />

	<h2 class="humaniterian-sub-heading">Help us raise money for our humaniterian causes</h2>

	<DonateButton text="Donate Now" href="/donate" ariaLabel="Donate to our cause" />
</section>

<style>
	.humaniterian-section {
		background:
			linear-gradient(to right, rgba(0, 0, 0, 0.9), rgba(0, 0, 0, 0.7)),
			url('../asserts/community-img.jpg') no-repeat center center/cover;
		height: auto;
		text-align: center;

		color: var(--text-color);
	}

	.humaniterian-sub-heading {
		font-size: 1.5rem;
		font-weight: 100;

		width: 100%;
		margin: 0 auto;

		margin-top: 3rem;
		margin-bottom: 3rem;
	}

	@media (min-width: 768px) {
		.humaniterian-sub-heading {
			font-size: 2rem;
			width: 70%;
		}
	}

	@media (min-width: 1024px) {
		.humaniterian-sub-heading {
			font-size: 2.5rem;
			width: 80%;
		}
	}

	@media (min-width: 1280px) {
		.humaniterian-sub-heading {
			font-size: 3rem;
			width: 60%;
		}
	}
</style>
