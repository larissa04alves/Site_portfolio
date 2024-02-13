<script lang="ts">
	import '../app.postcss';
	import { AppShell, AppBar } from '@skeletonlabs/skeleton';
	import Header from '$lib/assets/components/Header.svelte';

	// Floating UI for Popups
	import { computePosition, autoUpdate, flip, shift, offset, arrow } from '@floating-ui/dom';
	import { storePopup } from '@skeletonlabs/skeleton';
	import Sociais from '$lib/assets/components/Sociais.svelte';
	storePopup.set({ computePosition, autoUpdate, flip, shift, offset, arrow });
</script>

<AppShell>
	<Header />
	<!-- (sidebarLeft) -->

	<!-- (sidebarRight) -->
	<!-- (pageHeader) -->
	<!-- Router Slot -->
	<main class="flex h-full w-full">
		<Sociais />
		<div class="flex flex-col w-full"><slot /></div>
	</main>

	<!-- ---- / ---- -->
	<!-- (footer) -->
</AppShell>
