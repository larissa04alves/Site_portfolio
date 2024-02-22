<script lang="ts">
	import { TabGroup, Tab } from '@skeletonlabs/skeleton';

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
				<div class="flex flex-col gap-10"></div>
				<div class="flex flex-col gap-10"></div>
			</div>
		{:else if tabSet === 1}
			<div class="flex gap-10"></div>
		{:else if tabSet === 2}{:else if tabSet === 3}{/if}
	</svelte:fragment>
</TabGroup>
