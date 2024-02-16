<script lang="ts">
	import CardsProjetos from '$lib/assets/components/Cards_projetos.svelte';
	import Cards_projetos from '$lib/assets/components/Cards_projetos.svelte';

	let selectedTab = 1;
	let linePosition = 0;

	const tabs = [
		{ id: 1, text: 'Todos' },
		{ id: 2, text: 'Web' },
		{ id: 3, text: 'Mobile' },
		{ id: 4, text: 'Outros' }
	];

	const projects = [
		{
			id: 2,
			title: 'Tech Store',
			category: 'Website',
			technologies: 'HTML/CSS',
			description:
				'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut',
			image: '/src/lib/assets/img/techstore.svg'
		},
		{
			id: 4,
			title: 'School System',
			category: 'Java Application',
			technologies: 'Java, PostgreSQL, Java Swing',
			description:
				'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut',
			image: '/src/lib/assets/img/school.svg'
		},
		{
			id: 3,
			title: 'Habbit Tracker',
			category: 'Android Application',
			technologies: 'Flutter, Dart',
			description:
				'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut',
			image: '/src/lib/assets/img/habbit.svg'
		},
		{
			id: 2,
			title: 'Personal Portfólio',
			category: 'Website',
			technologies: 'Svelte, TypeScript',
			description:
				'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut',
			image: '/src/lib/assets/img/portfolio.svg'
		}
	];

	function selectTab(tab: number) {
		selectedTab = tab;
		linePosition = tab - 1;
	}

	function filterProjects(category: string | null): any[] {
		if (category === null) {
			return projects;
		} else {
			return projects.filter((project) => project.category === category);
		}
	}
</script>

<div>
	<ul class="tabs">
		{#each tabs as { id, text }}
			<li
				class="tab {selectedTab === id ? 'selected' : ''}"
				on:click={() => selectTab(id)}
				on:mouseover={() => (linePosition = id - 1)}
				on:mouseleave={() => (linePosition = selectedTab - 1)}
			>
				{text}
				{#if selectedTab === id}
					<div class={linePosition === id - 1 ? 'selected-tab-line' : ''}></div>
				{/if}
			</li>
		{/each}
	</ul>

	{#each filterProjects(selectedTab === 1 ? null : tabs[selectedTab - 1].text) as project (project.id)}
		<Cards_projetos {project} />
	{/each}
</div>

<style>
	.tabs {
		display: flex;
		list-style: none;
		position: relative;
		font-size: 1.3rem;
		font-weight: 600;
		gap: 3rem;
	}

	.tab {
		cursor: pointer;
		padding: 0.6rem;
		margin: 0 0.6rem;
		position: relative;
		user-select: none;
	}

	.tab:hover {
		border-bottom: 0.3rem solid #8c4de5;
		border-radius: 0.06rem;
	}

	.tab.selected {
		border-bottom: 0.3rem solid #8c4de5;
		border-radius: 0.06rem;
	}

	.selected-tab-line {
		background-color: #8c4de5;
	}

	.tab-content {
		margin-top: 1.3rem;
	}

	.title {
		font-size: 1.3rem;
		line-height: 3rem;
		font-weight: 500;
	}
	.card-container {
		width: 28rem;
		height: 16rem;
		position: relative;
		border-radius: 1rem;
		box-shadow: 0 0.9rem 1.3rem rgba(0, 0, 0, 0.2);
		overflow: hidden;
		flex-direction: column;
	}

	.card {
		width: 100%;
		height: 100%;
		border-radius: inherit;
	}

	.card .front-content {
		display: flex;
		flex-direction: column;
		padding: 1rem 0 0 2rem;
		font-size: 1.5rem;
		font-weight: 600;
		transition: all 0.6s cubic-bezier(0.23, 1, 0.32, 1);
	}
	.texto {
		font-size: 1.2rem;
		font-weight: 400;
	}

	.card .front-content p {
		font-size: 3rem;
		font-weight: 700;
		opacity: 1;
		background: linear-gradient(-45deg, #9675eb 0%, #7a5a99 100%);
		background-clip: text;
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		transition: all 0.6s cubic-bezier(0.23, 1, 0.32, 1);
	}

	.card .content {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		text-align: center;
		gap: 10px;
		background: linear-gradient(-45deg, #4f1ad5 0%, #9540e6 100%);
		color: #e8e8e8;
		padding: 20px;
		line-height: 1.5;
		border-radius: 5px;
		pointer-events: none;
		transform: translateX(-96%);
		transition: all 0.6s cubic-bezier(0.23, 1, 0.32, 1);
	}

	.card .content .heading {
		font-size: 32px;
		font-weight: 700;
	}

	.texto_tec {
		font-weight: 600;
	}

	.card:hover .content {
		transform: translateY(0);
	}

	.card:hover .front-content {
		transform: translateX(-30%);
	}

	.card:hover .front-content p {
		opacity: 0;
	}
</style>
