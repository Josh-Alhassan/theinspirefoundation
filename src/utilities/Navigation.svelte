<script lang="ts">
	import logo from '../asserts/logo.png';
	export let links: Array<{ href: string; text: string }> = [
		{ href: '/', text: 'Home' },
		{ href: '/about', text: 'About' },
		{ href: '/services', text: 'Services' },
		{ href: '/contact', text: 'Contact' },
		{ href: '/donate', text: 'Donate' }
	];

	let mobileMenuOpen = false;
	let isMobile = false;

	import { onMount } from 'svelte';

	onMount(() => {
		const checkMobile = () => {
			isMobile = window.innerWidth < 768;
			if (!isMobile) mobileMenuOpen = false;
		};

		checkMobile();
		window.addEventListener('resize', checkMobile);

		return () => window.removeEventListener('resize', checkMobile);
	});

	function toggleMobileMenu() {
		mobileMenuOpen = !mobileMenuOpen;
	}
</script>

<nav class="navigation" aria-label="Main navigation">
	<div class="container">
		<!-- Logo/Brand -->
		<a href="/" class="brand">
			<img src={logo} alt="Logo" class="logo" aria-label="Logo" loading="lazy" />
		</a>

		<!-- Desktop Navigation -->
		<ul class="desktop-nav">
			{#each links as link}
				<li>
					<a href={link.href} class="nav-link">{link.text}</a>
				</li>
			{/each}
		</ul>

		<!-- Mobile Menu Button -->
		<button
			class="mobile-menu-button"
			on:click={toggleMobileMenu}
			aria-expanded={mobileMenuOpen}
			aria-label="Toggle navigation menu"
		>
			<span class="hamburger {mobileMenuOpen ? 'open' : ''}">
				<span class="line"></span>
				<span class="line"></span>
				<span class="line"></span>
			</span>
		</button>
	</div>

	<!-- Mobile Navigation (Overlay) -->
	{#if mobileMenuOpen}
		<!-- svelte-ignore a11y_click_events_have_key_events -->
		<!-- svelte-ignore a11y_no_static_element_interactions -->
		<div class="mobile-nav-overlay" on:click|self={toggleMobileMenu}>
			<ul class="mobile-nav">
				{#each links as link}
					<li>
						<a href={link.href} class="nav-link" on:click={() => (mobileMenuOpen = false)}>
							{link.text}
						</a>
					</li>
				{/each}
			</ul>
		</div>
	{/if}
</nav>

<style>
	.navigation {
		background-color: var(--secondary-color-trans);
		box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
		position: relative;
		z-index: 100;
	}

	.container {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 1rem 2rem;
	}

	.logo {
		width: 100px;
		height: 100px;
		border-radius: 50%;
		object-fit: cover;
	}

	.brand {
		font-weight: bold;
		font-size: 1.25rem;
		text-decoration: none;
		color: var(--text-color);
	}

	.desktop-nav {
		display: none;
		list-style: none;
		margin: 0;
		padding: 0;
		gap: 1.5rem;
	}

	.nav-link {
		text-decoration: none;
		color: var(--nav-text, #333333);
		font-weight: 500;
		padding: 0.5rem 0;
		position: relative;
		transition: color 0.2s ease;
	}

	.desktop-nav .nav-link {
		color: var(--text-color);
	}

	.nav-link:hover {
		color: var(--nav-accent, #0066cc);
	}

	.nav-link::after {
		content: '';
		position: absolute;
		bottom: 0;
		left: 0;
		width: 0;
		height: 2px;
		background-color: var(--nav-accent, #0066cc);
		transition: width 0.3s ease;
	}

	.nav-link:hover::after {
		width: 100%;
	}

	.mobile-menu-button {
		background: none;
		border: none;
		cursor: pointer;
		padding: 0.5rem;
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.hamburger {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		width: 24px;
		height: 18px;
	}

	.line {
		height: 2px;
		width: 100%;
		background-color: var(--text-color);
		transition: all 0.3s ease;
	}

	.hamburger.open .line:nth-child(1) {
		transform: translateY(8px) rotate(45deg);
	}

	.hamburger.open .line:nth-child(2) {
		opacity: 0;
	}

	.hamburger.open .line:nth-child(3) {
		transform: translateY(-8px) rotate(-45deg);
	}

	.mobile-nav-overlay {
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		background-color: rgba(0, 0, 0, 0.5);
		z-index: 99;
		display: flex;
		justify-content: flex-end;
	}

	.mobile-nav {
		list-style: none;
		margin: 0;
		padding: 2rem;
		background-color: var(--nav-bg, #ffffff);
		width: 70%;
		max-width: 300px;
		height: 100vh;
		display: flex;
		flex-direction: column;
		gap: 1.5rem;
		animation: slideIn 0.3s ease-out;
	}

	@keyframes slideIn {
		from {
			transform: translateX(100%);
		}
		to {
			transform: translateX(0);
		}
	}

	@media (min-width: 768px) {
		.desktop-nav {
			display: flex;
		}

		.mobile-menu-button {
			display: none;
		}
	}

	@media (min-width: 1024px) {
		.container {
			padding: 1.5rem 4rem;
		}
	}

	@media (min-width: 1920px) {
		.container {
			max-width: 1920px;
			margin: 0 auto;
		}
	}
</style>
