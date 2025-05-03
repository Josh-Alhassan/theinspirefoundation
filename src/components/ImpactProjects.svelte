<script>
	import projectImg1 from '../asserts/project-img-1.jpg';
	import projectImg2 from '../asserts/project-img-2.jpg';
	import projectImg3 from '../asserts/project-img-3.jpg';

	const projects = [
		{
			image: projectImg1,
			alt: 'Education project',
			tag: 'Education',
			description: 'Education programmes that lorems ipsum...'
		},
		{
			image: projectImg2,
			alt: 'Health Care',
			tag: 'Health Care',
			description: 'Free counseling lorems ipsum odio sit ullameo...'
		},
		{
			image: projectImg3,
			alt: 'Awareness',
			tag: 'Awareness',
			description: 'Local community forum lorem ipsum odio sit...'
		}
	];
</script>

<div class="impact-projects">
	{#each projects as project}
		<a href="#" class="projects-container">
			<div class="projects-img">
				<img src={project.image} alt={project.alt} class="impact-img" loading="lazy" />
			</div>
			<h4 class="project-tag">{project.tag}</h4>
			<h3 class="project-description">{project.description}</h3>
		</a>
	{/each}
</div>

<style>
	.impact-projects {
		/* background-color: var(--secondary-color-trans); */
		padding: 1rem;
		margin-top: 2rem;

		display: flex;
		flex-wrap: wrap;
		column-gap: 2rem;
	}

	.projects-container {
		display: flex;
		flex-direction: column;
		max-width: 100%;
		color: var(--text-color-dark);
		cursor: pointer;

		margin-bottom: 3rem;
	}

	.impact-img {
		width: 100%;
		height: auto;
		object-fit: cover;
		border-radius: 5px;
	}

	.project-tag {
		text-transform: uppercase;
		font-weight: 600;
		border-bottom: 2px solid var(--text-color-dark);
		padding: 0.5rem 0;
	}

	.project-description {
		font-size: 1rem;
		font-weight: 400;
		margin-top: 1.5rem;
	}

	@media (min-width: 768px) {
		.impact-projects {
			justify-content: center;
		}

		.project-tag {
			font-size: 1rem;
		}

		.project-description {
			font-size: 1.2rem;
		}
	}

	@media (min-width: 1024px) {
		.impact-projects {
			justify-content: start;
		}

		.projects-container {
			max-width: 350px;
		}

		.project-tag {
			font-size: 1.3rem;
		}

		.project-description {
			font-size: 1.5rem;
		}
	}

	@media (min-width: 1280px) {
		.impact-projects {
			justify-content: start;
		}
	}
</style>
