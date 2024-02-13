<script>
	import personagem from '$lib/assets/img/personagem.svg';
</script>

<section class="heroSection w-full py-10">
	<div class="texto">
		<h3 class="text-4xl font-semibold">Oi!</h3>
		<h1 class="text-6xl font-semibold">Sou <span class="nameColor">Larissa Alves</span></h1>
		<h2 class="text-5xl font-semibold">Software Developer</h2>
		<button class="btn">Download CV</button>
	</div>
	<div>
		<img class="image" src={personagem} alt="imagem hero" />
	</div>
</section>

<style>
	.heroSection {
		display: flex;
		justify-content: space-around;
	}
	.texto {
		padding: 130px 0 20px 0;
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
		font-weight: 700;
		position: absolute;
		left: 160px;
	}
</style>
