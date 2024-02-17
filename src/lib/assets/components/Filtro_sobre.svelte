<script lang="ts">
	import { TabGroup, Tab } from '@skeletonlabs/skeleton';
	let tabSet: number = 0;
</script>

<TabGroup
	justify="justify-evenly"
	rounded="none"
	hover="hover:none"
	active="border-b-4 border-primary-500"
	regionList="border-b-0 "
	regionPanel="border-none"
>
	<Tab regionTab="font-semibold text-xl" bind:group={tabSet} name="tab1" value={0}>Skills</Tab>
	<Tab regionTab="font-semibold text-xl" bind:group={tabSet} name="tab2" value={1}>Experiência</Tab>
	<Tab regionTab="font-semibold text-xl" bind:group={tabSet} name="tab3" value={2}>Educação</Tab>
	<Tab regionTab="font-semibold text-xl" bind:group={tabSet} name="tab3" value={3}>Certificados</Tab
	>
	<!-- Tab Panels --->
	<svelte:fragment slot="panel">
		{#if tabSet === 0}
			<h1 class="title">Backend Development</h1>
			<p class="info">Java, Python, Dart, PostgreSQL</p>
			<h1 class="title">Frontend Development</h1>
			<p class="info">Svelte, HTML/CSS</p>
			<h1 class="title">Mobile Development</h1>
			<p class="info">Flutter</p>
		{:else if tabSet === 1}
			<h1 class="title">Assistente de Dados</h1>
			<h1 class="info">out/2023 - atualmente</h1>
			<p class="info">UNIVATES</p>
		{:else if tabSet === 2}
			<h1 class="title">Engenharia de Software</h1>
			<h1 class="info">2023 - atualmente</h1>
			<p class="info">UNIVATES</p>
		{:else if tabSet === 3}
			<h1 class="title">Power BI - Básico ao Avançado</h1>
			<h1 class="info">jan/2023</h1>
			<p class="info">Udemy</p>
		{/if}
	</svelte:fragment>
</TabGroup>

<style>
	.tabs {
		font-size: 1.3rem;
		line-height: 3rem;
		font-weight: 700;
	}

	.title {
		font-size: 1.3rem;
		line-height: 3rem;
		font-weight: 500;
	}
</style>
