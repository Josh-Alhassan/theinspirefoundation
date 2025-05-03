<script lang="ts">
	export let href: string = '/donate';
	export let text: string = 'Donate';
	// export let primaryColor: string = 'var(--primary-color)';
	// export let textColor: string = 'var(--text-color)';
	// export let padding: string = '0.5rem 1.5rem';
	// export let borderRadius: string = '5px';
	export let ariaLabel: string = 'Make a donation';
</script>

<a {href} class="donate-btn" aria-label={ariaLabel}>{text}</a>

<style>
	.donate-btn {
		background-color: var(--primary-color);
		color: var(--text-color);
		padding: 0.5rem 1.5rem;
		border-radius: 5px;
		font-size: 1rem;
		font-weight: 500;
	}

	@media (min-width: 768px) {
		.donate-btn {
			font-size: 1.2rem;
			padding: 0.5rem 2rem;
		}
	}

	@media (min-width: 1024px) {
		.donate-btn {
			font-size: 1.5rem;
			padding: 0.5rem 2.5rem;
		}
	}

	/* @media (max-width: 1024px) {
		.donate-btn {
			font-size: 1rem;
		}
	} */
</style>
