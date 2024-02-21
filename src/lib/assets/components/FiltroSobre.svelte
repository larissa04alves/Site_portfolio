<script lang="ts">
	import { TabGroup, Tab } from '@skeletonlabs/skeleton';
	let tabSet: number = 0;
</script>

<TabGroup
	justify="justify-start"
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
			<h1 class="text-xl">Backend Development</h1>
			<p>Java, Python, Dart, PostgreSQL</p>
			<h1 class="text-xl">Frontend Development</h1>
			<p>Svelte, HTML/CSS</p>
			<h1 class="text-xl">Mobile Development</h1>
			<p>Flutter</p>
		{:else if tabSet === 1}
			<h1 class="text-xl">Assistente de Dados</h1>
			<h1>out/2023 - atualmente</h1>
			<p>UNIVATES</p>
		{:else if tabSet === 2}
			<h1 class="text-xl">Engenharia de Software</h1>
			<h1>2023 - atualmente</h1>
			<p>UNIVATES</p>
		{:else if tabSet === 3}
			<h1 class="text-xl">Power BI - Básico ao Avançado</h1>
			<h1>jan/2023</h1>
			<p>Udemy</p>
		{/if}
	</svelte:fragment>
</TabGroup>
