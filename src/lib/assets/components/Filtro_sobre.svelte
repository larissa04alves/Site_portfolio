<script lang="ts">
	let selectedTab = 1;
	let linePosition = 0;

	const tabs = [
		{ id: 1, text: 'Skills' },
		{ id: 2, text: 'Experiência' },
		{ id: 3, text: 'Educação' },
		{ id: 4, text: 'Certificados' }
	];

	function selectTab(tab: number) {
		selectedTab = tab;
		linePosition = tab - 1;
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

	{#if selectedTab == 1}
		<div class="tab-content">
			<h1 class="title">Backend Development</h1>
			<p class="info">Java, Python, Dart, PostgreSQL</p>
			<h1 class="title">Frontend Development</h1>
			<p class="info">Svelte, HTML/CSS</p>
			<h1 class="title">Mobile Development</h1>
			<p class="info">Flutter</p>
		</div>
	{/if}
	{#if selectedTab == 2}
		<div class="tab-content">
			<h1 class="title">Assistente de Dados</h1>
			<h1 class="info">out/2023 - atualmente</h1>
			<p class="info">UNIVATES</p>
		</div>
	{/if}
	{#if selectedTab == 3}
		<div class="tab-content">
			<h1 class="title">Engenharia de Software</h1>
			<h1 class="info">2023 - atualmente</h1>
			<p class="info">UNIVATES</p>
		</div>
	{/if}
	{#if selectedTab == 4}
		<div class="tab-content">
			<h1 class="title">Power BI - Básico ao Avançado</h1>
			<h1 class="info">jan/2023</h1>
			<p class="info">Udemy</p>
		</div>
	{/if}
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
</style>
