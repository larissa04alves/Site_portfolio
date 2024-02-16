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
		<div class="linha"></div>
	</div>
	<div class="linha"></div>
	<div class="texto">
		<h1>Made by <span class="name">Larissa Alves</span></h1>
		<p>&copy; 2023 Larissa Alves. All rights reserved</p>
	</div>
</section>

<style>
	section {
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		width: 100%;
		height: 12rem;
		background-color: #3a3a3a;
	}
	.logos {
		display: flex;
		padding-bottom: 1rem;
		flex-direction: row;
		gap: 1.25rem;
	}
	.logo {
		width: 2rem;
	}
	.texto {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 0.1rem;
		padding-top: 1rem;
	}
	.name {
		font-weight: 600;
		font-size: 1.2rem;
	}
	.linha {
		width: 60%;
		border-bottom: 1px solid #ffffff;
	}
</style>
