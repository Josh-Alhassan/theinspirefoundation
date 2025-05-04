<script>
	import DonateButton from '../utilities/DonateButton.svelte';
</script>

<section class="events-cards section-padding">
	<div class="events-cards-container">
		<div class="events-card">
			<date class="events-card__date">17 July, 2020</date>
			<h3 class="events-card__title">Education Program that lorem ipsum</h3>
			<p class="events-card__description">
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis quibusdam possimus
				quisquam, dolore nemo sapiente exercitationem. Quos, corrupti ducimus repellendus voluptas
				fugiat, porro, voluptatem hic fugit harum cupiditate ea debitis.
			</p>

			<DonateButton text="Read More" href="/read-more" ariaLabel="Read more about our events" />
		</div>

		<div class="events-card">
			<date class="events-card__date">17 July, 2020</date>
			<h3 class="events-card__title">Education Program that lorem ipsum</h3>
			<p class="events-card__description">
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis quibusdam possimus
				quisquam, dolore nemo sapiente exercitationem. Quos, corrupti ducimus repellendus voluptas
				fugiat, porro, voluptatem hic fugit harum cupiditate ea debitis.
			</p>

			<DonateButton text="Read More" href="/read-more" ariaLabel="Read more about our events" />
		</div>

		<div class="events-card">
			<date class="events-card__date">17 July, 2020</date>
			<h3 class="events-card__title">Education Program that lorem ipsum</h3>
			<p class="events-card__description">
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis quibusdam possimus
				quisquam, dolore nemo sapiente exercitationem. Quos, corrupti ducimus repellendus voluptas
				fugiat, porro, voluptatem hic fugit harum cupiditate ea debitis.
			</p>

			<DonateButton text="Read More" href="/read-more" ariaLabel="Read more about our events" />
		</div>
	</div>
</section>

<style>
	.events-cards {
		background-color: var(--primary-color-opacity);
	}
	.events-cards-container {
		display: flex;
		/* flex-direction: column; */
		flex-wrap: wrap;
		gap: 2rem;
		row-gap: 4rem;
		margin: 0 auto;
		margin: 4rem 0;
	}

	.events-card {
		width: 100%;
	}

	.events-card__date {
		font-size: 0.8rem;
		text-transform: uppercase;
		padding-bottom: 0.5rem;
		border-bottom: 3px solid var(--text-color-dark);

		display: block;
	}

	.events-card__title {
		padding-top: 2rem;
		font-size: 1.5rem;
		line-height: 1.2;
		font-weight: 100;
	}

	.events-card__description {
		margin-top: 1rem;
		margin-bottom: 2.5rem;
		font-size: 1rem;
		text-align: justify;
	}

	@media (min-width: 768px) {
		.events-card {
			width: 300px;
		}
	}

	@media (min-width: 1024px) {
		.events-cards-container {
			justify-content: space-between;
		}

		.events-card {
			width: 250px;
		}
	}

	@media (min-width: 1440px) {
		.events-cards-container {
			justify-content: space-between;
		}

		.events-card {
			width: 350px;
		}
	}

	@media (min-width: 1920px) {
		.events-cards-container {
			max-width: 1920px;
			margin: 0 auto;

			justify-content: center;
			gap: 4rem;
		}
	}
</style>
