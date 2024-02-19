<script>
	import logo_X from '$lib/assets/img/logo_X.svg';
	import logo_instagram from '$lib/assets/img/logo_instagram.svg';
	import logo_linkedin from '$lib/assets/img/logo_linkedin.svg';
	import logo_GiHub from '$lib/assets/img/logo_GiHub.svg';
</script>

<section>
	<div class="logos">
		<a target="_blank" href="https://x.com/_Lari_alvess?t=99Cv58aJzrQao2cahTrOaQ&s=09">
			<img class="logo" src={logo_X} alt="Logo" />
		</a>

		<a target="_blank" href="https://www.instagram.com/_alvesslari?igsh=MXZtaHRlcThhYThmaA==">
			<img class="logo" src={logo_instagram} alt="Logo" />
		</a>
		<a target="_blank" href="https://www.linkedin.com/in/larissa-alves-069944286/">
			<img class="logo" src={logo_linkedin} alt="Logo" />
		</a>
		<a target="_blank" href="https://github.com/larissa04alves">
			<img class="logo" src={logo_GiHub} alt="Logo" />
		</a>
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
