<script lang="ts">
	import logo from '$lib/assets/img/logo.svg';
</script>

<header
	class="px-[0.2rem] flex justify-around lg:fixed bg-surface-900 w-full items-center py-[0.4rem] z-50 shadow-md shadow-secondary-800"
>
	<a href="/" class="min-w-20">
		<img class="w-[7rem] lg:w-[9.6rem] min-w-20" src={logo} alt="Logo" />
	</a>

	<nav class="hidden lg:flex gap-12 font-semibold text-base">
		<a class="animado relative no-underline" href="/">Home</a>
		<a class="animado relative no-underline" href="#sobre">Sobre</a>
		<a class="animado relative no-underline" href="#portfolio">Portfólio</a>
	</nav>
	<a href="/contato">
		<button
			class=" btn border-2 border-primary-600 rounded-[0.8rem] py-[0.3rem] px-[1.6rem] decoration-secundary-100 font-semibold"
		>
			Contato
		</button>
	</a>
</header>

<style>
	.animado::before {
		content: '';
		position: absolute;
		width: 100%;
		height: 0.25rem;
		border-radius: 0.13rem;
		background-color: #a666ff;
		bottom: 0;
		left: 0;
		transform-origin: right;
		transform: scaleX(0);
		transition: transform 0.2s ease-in-out;
	}
	.animado:hover::before {
		transform-origin: left;
		transform: scaleX(1);
	}
	.animado:focus::before {
		transform-origin: left;
		transform: scaleX(1);
	}

	.btn:hover {
		background-color: #3f1397;
		border: 0.06rem solid #3f1397;
	}
</style>
