<script>
	import DonateButton from './DonateButton.svelte';
</script>

<div class="events-donation">
	<p class="events-description">Help us raise money for lorem ipsum</p>

	<div class="events-donation-btn">
		<DonateButton text="Donate" href="/donate" ariaLabel="Donate to our events" />
	</div>
</div>

<style>
	.events-donation {
		width: 100%;
		height: auto;
		padding: 3rem;
		color: var(--text-color);

		background:
			linear-gradient(to right, rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.7)),
			url('../asserts/donation-img.jpg') no-repeat center center/cover;
	}

	.events-description {
		font-size: 1.5rem;
		line-height: 1.2;
		text-align: center;
		font-weight: 100;

		margin-bottom: 3rem;
	}

	.events-donation-btn {
		display: flex;
		align-items: center;
		justify-content: center;
	}

	@media (min-width: 1024px) {
		.events-donation {
			width: 400px;
		}
	}
	/* @media (min-width: 1920px) {
		.about-us {
			max-width: 1920px;
			margin: 0 auto;
		}
	} */
</style>
