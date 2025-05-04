<script>
	export let text = '';
	export let highlightedText = '';
	export let highlightUnderline = true;
	export let highlightBold = true;
</script>

<h3 class="tertiary-heading">
	{text}
	{#if highlightedText}
		<span class="highlight" class:underline={highlightUnderline} class:bold={highlightBold}>
			{highlightedText}
		</span>
	{/if}
</h3>

<style>
	.tertiary-heading {
		font-size: 1.5rem;
		line-height: 1.1;
		color: var(--text-color-dark);
		font-weight: 400;
		margin-bottom: 1.5rem;
	}

	.highlight {
		color: inherit;
	}

	.underline {
		text-decoration: underline;
	}

	.bold {
		font-weight: 600;
	}

	@media (min-width: 768px) {
		.tertiary-heading {
			font-size: 2rem;
		}
	}

	@media (min-width: 1024px) {
		.tertiary-heading {
			font-size: 2.5rem;
		}
	}
</style>
