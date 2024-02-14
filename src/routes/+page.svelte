<script>
	import personagem from '$lib/assets/img/personagem.svg';
	import my_image from '$lib/assets/img/my_image.png';
	import FiltroSobre from '$lib/assets/components/Filtro_sobre.svelte';
</script>

<section id="1" class="heroSection">
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

<section id="2" class="sobre">
	<div>
		<img class="minha_foto" src={my_image} alt="minha foto" />
	</div>

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

<style>
	.heroSection {
		display: flex;
		justify-content: space-around;
		width: 100%;
		padding: 80px 0 80px 0;
	}
	.texto {
		padding: 70px 20px 0;
		position: relative;
	}
	.nameColor {
		font-weight: 700;
		background: linear-gradient(#ccb4ee, rgba(164, 105, 247, 0.631), #6518d1);
		background-clip: text;
		color: transparent;
	}
	.btn {
		margin-top: 30px;
		border-radius: 12px;
		padding: 10px 20px;
		background: linear-gradient(rgba(164, 105, 247, 0.631), #6518d1);
		font-weight: 600;
		position: absolute;
		left: 160px;
	}
	.sobre {
		display: flex;
		width: 100%;
		height: 35rem;
		background-color: #3a3a3a;
		padding: 40px 120px 0 120px;
	}
	.minha_foto {
		width: 600px;
		border-radius: 15px;
	}
	.texto_sobre {
		display: flex;
		flex-direction: column;
		justify-content: flex-start;
		padding: 10px 0 0 60px;
	}
	.titulo {
		font-size: 40px;
		line-height: normal;
		font-weight: 500;
	}
	.texto_geral {
		font-size: 16px;
		font-weight: 400;
	}

	.filtro {
		margin-top: 20px;
	}
</style>
