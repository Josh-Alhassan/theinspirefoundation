<script>
	// This is a simple navigation component for a website.
	// It includes links to various sections of the site.
	// The component is styled to be responsive and user-friendly.
	// The logo is displayed on the left, and the navigation links are on the right.

	// The navigation bar is designed to be fixed at the top of the page for easy access.
	// import '../app.css';
</script>

<nav class="navbar section-padding">
	<img src="/logo.png" alt="Logo" class="logo" />

	<div class="nav-links-container">
		<ul class="nav-links">
			<li class="class-link"><a href="/">Home</a></li>
			<li class="class-link"><a href="/about">About Us</a></li>
			<li class="class-link"><a href="/contact">What we do</a></li>
			<li class="class-link"><a href="/contact">Events</a></li>
			<li class="class-link"><a href="/contact">Gallery</a></li>
			<li class="class-link"><a href="/contact">Contacts</a></li>
		</ul>

		<a href="/donate" class="donate-btn">Donate</a>
	</div>
</nav>

<style>
	.navbar {
		display: flex;
		align-items: center;
		justify-content: space-between;
		background-color: var(--secondary-color-trans);
		padding: 1rem 4rem;
	}
	.logo {
		width: 50px;
		height: auto;
		margin-right: 20px;
	}

	.nav-links-container {
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 2rem;
	}
	ul {
		display: flex;
		gap: 1.6rem;
	}
	a {
		color: white;
		text-decoration: none;
		font-size: 1.2rem;
	}
	a:hover {
		text-decoration: underline;
	}

	.donate-btn {
		background-color: var(--primary-color);
		color: var(--text-color);
		padding: 0.5rem 1.5rem;
		border-radius: 5px;
	}
</style>
