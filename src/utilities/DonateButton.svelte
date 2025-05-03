<script lang="ts">
	export const href: string = '/donate';
	export const text: string = 'Donate';
	export const primaryColor: string = 'var(--primary-color)';
	export const textColor: string = 'var(--text-color)';
	export const padding: string = '0.5rem 1.5rem';
	export const borderRadius: string = '5px';
	export const ariaLabel: string = 'Make a donation';
</script>

<a {href} class="donate-btn" aria-label={ariaLabel}>{text}</a>

<style>
	.donate-btn {
		background-color: var(--primary-color);
		color: var(--text-color);
		padding: 0.5rem 1.5rem;
		border-radius: 5px;
	}

	@media (max-width: 1024px) {
		.donate-btn {
			font-size: 1rem;
		}
	}
</style>
