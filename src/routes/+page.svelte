<script>
	import personagem from '$lib/assets/img/personagem.svg';
	import my_image from '$lib/assets/img/my_image.jpeg';
	import FiltroSobre from '$lib/assets/components/FiltroSobre.svelte';
	import Filtro_portfolio from '$lib/assets/components/FiltroPortfolio.svelte';
	import Sociais from '$lib/assets/components/Sociais.svelte';
</script>

<section class="heroSection">
	<div class="sociais">
		<Sociais />
	</div>
	<div class="texto">
		<h3 class="text-4xl font-semibold">Oi!</h3>
		<h1 class="text-6xl font-semibold">Sou <span class="nameColor">Larissa Alves</span></h1>
		<h2 class="text-5xl font-semibold">Software Developer</h2>
		<a
			target="_blank"
			href="https://drive.google.com/file/d/1cL3zs477zX99xxtpi3qUZFjSej4Ktw9c/view?usp=sharing"
		>
			<button class="btn">Download CV</button>
		</a>
	</div>
	<div>
		<img class="image" src={personagem} alt="imagem hero" />
	</div>
</section>

<section id="sobre" class="sobre">
	<img class="hidden md:flex minha_foto" src={my_image} alt="minha foto" />

	<div class="texto_sobre">
		<h1 class="titulo">Sobre mim</h1>
		<p class="texto_geral">
			Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
			labore et dolore magna aliqua.
		</p>
		<p class="texto_geral">
			Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
			commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum
			dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa
			qui officia deserunt mollit anim id est laborum
		</p>
		<div class="filtro">
			<FiltroSobre />
		</div>
	</div>
</section>
<section id="portfolio" class="portfolio">
	<div class="texto_port">
		<h1 class="titulo_port">Portfólio</h1>
		<h3>Meus Projetos Recentes</h3>
	</div>
	<div class="cards">
		<Filtro_portfolio />
	</div>
</section>

<style>
	.heroSection {
		display: flex;
		justify-content: space-between;
		width: 100%;
		padding: 6rem 8rem 6rem 0;
	}
	.texto {
		padding: 7rem 2rem 0;
		position: relative;
	}
	.nameColor {
		font-weight: 700;
		background: linear-gradient(#ccb4ee, rgba(164, 105, 247, 0.631), #6518d1);
		background-clip: text;
		color: transparent;
	}
	.btn {
		margin-top: 2rem;
		border-radius: 0.8rem;
		padding: 0.6rem 1.3rem;
		background: linear-gradient(rgba(164, 105, 247, 0.631), #6518d1);
		font-weight: 600;
		position: absolute;
		left: 10rem;
	}
	.sociais {
		display: flex;
		justify-content: flex-end;
		right: 0;
		top: 0;
		padding: 2rem;
	}
	.sobre {
		display: flex;
		width: 100%;
		height: 35rem;
		background-color: #3a3a3a;
		padding: 1.5rem 8rem;
	}

	.minha_foto {
		border-radius: 1rem;
	}
	.texto_sobre {
		display: flex;
		flex-direction: column;
		padding-left: 3rem;
	}
	.titulo {
		font-size: 2.5rem;
		line-height: normal;
		font-weight: 500;
	}
	.texto_geral {
		font-size: 1rem;
		font-weight: 400;
	}

	.filtro {
		margin-top: 1.5rem;
	}

	.portfólio {
		width: 100%;
		height: 100%;
	}
	.texto_port {
		display: flex;
		flex-direction: column;
		align-items: center;
		font-weight: 600;
	}
	.titulo_port {
		font-size: 2.5rem;
		line-height: normal;
		font-weight: 500;
		padding: 4rem 0 0.3rem 0;
	}
	.cards {
		display: flex;
		justify-content: center;
		padding-bottom: 4rem;
	}
</style>
