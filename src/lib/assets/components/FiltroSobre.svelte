<script lang="ts">
	import { TabGroup, Tab } from '@skeletonlabs/skeleton';
	import { dataSobre } from '$lib/assets/data/dataSobre.js';
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
			{#each dataSobre.Skills as skill}
				<h1 class="text-xl font-semibold">{skill.title}</h1>
				<p class="pb-2">{skill.description}</p>
			{/each}
		{:else if tabSet === 1}
			{#each dataSobre.Experiencia as experiencia}
				<h1 class="text-xl font-semibold">{experiencia.title}</h1>
				<h1>{experiencia.date}</h1>
				<p>{experiencia.organization}</p>
			{/each}
		{:else if tabSet === 2}
			{#each dataSobre.Educacao as educacao}
				<h1 class="text-xl font-semibold">{educacao.title}</h1>
				<h1>{educacao.date}</h1>
				<p>{educacao.organization}</p>
			{/each}
		{:else if tabSet === 3}
			{#each dataSobre.Certificados as certificado}
				<h1 class="text-xl font-semibold">{certificado.title}</h1>
				<h1>{certificado.date}</h1>
				<p>{certificado.organization}</p>
			{/each}
		{/if}
	</svelte:fragment>
</TabGroup>
