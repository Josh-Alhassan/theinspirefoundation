<script lang="ts">
	export let href: string = '/donate';
	export let text: string = 'Donate';
	export let primaryColor: string = 'var(--primary-color)';
	export let textColor: string = 'var(--text-color)';
	export let padding: string = '0.5rem 1.5rem';
	export let borderRadius: string = '5px';
	export let ariaLabel: string = 'Make a donation';
</script>

<a {href} class="donate-btn" aria-label={ariaLabel}>{text}</a>

<style>
	.donate-btn {
		background-color: var(--primary-color);
		color: var(--text-color);
		padding: 0.5rem 1.5rem;
		border-radius: 5px;
	}
</style>
