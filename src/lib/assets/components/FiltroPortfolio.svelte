<script lang="ts">
	import { TabGroup, Tab, TabAnchor } from '@skeletonlabs/skeleton';
	import Project1 from '$lib/assets/components/Project1.svelte';
	import Project2 from './Project2.svelte';
	import Project3 from './Project3.svelte';
	import Project4 from './Project4.svelte';

	let tabSet: number = 0;
</script>

<TabGroup
	justify="justify-center"
	rounded="none"
	hover="hover:none"
	active="border-b-4 border-primary-500"
	regionList="border-b-0 "
	regionPanel="border-none  "
	padding="px-10 py-2"
	class="flex flex-col justify-center items-center"
>
	<Tab regionTab="font-bold text-xl" bind:group={tabSet} name="tab1" value={0}>Todos</Tab>
	<Tab regionTab="font-bold text-xl" bind:group={tabSet} name="tab2" value={1}>Web</Tab>
	<Tab regionTab="font-bold text-xl" bind:group={tabSet} name="tab3" value={2}>Mobile</Tab>
	<Tab regionTab="font-bold text-xl" bind:group={tabSet} name="tab3" value={3}>Outros</Tab>
	<!-- Tab Panels --->
	<svelte:fragment slot="panel">
		{#if tabSet === 0}
			<div class="flex w-full gap-10">
				<div class="flex flex-col gap-10">
					<Project1 />
					<Project2 />
				</div>
				<div class="flex flex-col gap-10">
					<Project3 />
					<Project4 />
				</div>
			</div>
		{:else if tabSet === 1}
			<div class="flex gap-10">
				<Project1 />
				<Project4 />
			</div>
		{:else if tabSet === 2}
			<Project3 />
		{:else if tabSet === 3}
			<Project2 />
		{/if}
	</svelte:fragment>
</TabGroup>
