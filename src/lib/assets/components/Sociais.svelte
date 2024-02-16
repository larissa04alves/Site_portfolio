<script>
	import logo_X from '$lib/assets/img/logo_X.svg';
	import logo_instagram from '$lib/assets/img/logo_instagram.svg';
	import logo_linkedin from '$lib/assets/img/logo_linkedin.svg';
	import logo_GiHub from '$lib/assets/img/logo_GiHub.svg';
</script>

<section>
	<div class="logos">
		<img class="logo" src={logo_X} alt="Logo" />
		<img class="logo" src={logo_instagram} alt="Logo" />
		<img class="logo" src={logo_linkedin} alt="Logo" />
		<img class="logo" src={logo_GiHub} alt="Logo" />
	</div>
</section>

<style>
	.logos {
		display: flex;
		flex-direction: column;
		gap: 1.25rem;
	}
	.logo {
		width: 2rem;
	}
</style>
