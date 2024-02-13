<script>
	import logo_X from '$lib/assets/img/logo_X.svg';
	import logo_instagram from '$lib/assets/img/logo_instagram.svg';
	import logo_linkedin from '$lib/assets/img/logo_linkedin.svg';
	import logo_GiHub from '$lib/assets/img/logo_GiHub.svg';
</script>

<section class=" h-full flex items-end justify-end absolute">
	<div class="logos">
		<img src={logo_X} alt="Logo" />
		<img src={logo_instagram} alt="Logo" />
		<img src={logo_linkedin} alt="Logo" />
		<img src={logo_GiHub} alt="Logo" />
		<div class="linha w-1/2"></div>
	</div>
</section>

<style>
	section {
		display: flex;
		height: full;
		justify-content: flex-end;
		align-items: flex-end;
		position: absolute;
	}
	.logos {
		display: flex;
		flex-direction: column;
		padding: 0 40px;
		gap: 1.25rem;
	}
	.linha {
		border-right: 1px solid #828282;
		height: 300px;
	}
</style>
