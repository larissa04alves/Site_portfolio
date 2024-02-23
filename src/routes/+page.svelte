<script>
	import FiltroSobre from '$lib/assets/components/FiltroSobre.svelte';
	import Filtro_portfolio from '$lib/assets/components/FiltroPortfolio.svelte';
	import Sociais from '$lib/assets/components/Sociais.svelte';

	import favicon from '$lib/assets/img/favicon.svg';
	import my_image from '$lib/assets/img/my_image.jpeg';
	import personagem from '$lib/assets/img/personagem.svg';
</script>

<head>
	<link rel="icon" href={favicon} />
</head>

<section class=" flex justify-between w-full py-[10rem] pr-[12rem]">
	<div class="flex items-center px-[2rem]">
		<Sociais />
	</div>
	<div class="relative py-[7rem] px-[2rem]">
		<h3 class="text-5xl font-semibold">Oi!</h3>
		<h1 class="text-7xl font-semibold">
			Sou <span
				class="font-bold bg-clip-text text-transparent bg-gradient-to-r from-purple-500 via-purple-800 to-purple-600"
				>Larissa Alves</span
			>
		</h1>
		<h2 class="text-6xl font-semibold">Software Developer</h2>
		<a
			target="_blank"
			href="https://drive.google.com/file/d/1cL3zs477zX99xxtpi3qUZFjSej4Ktw9c/view?usp=sharing"
		>
			<button
				class="flex relative left-[10rem] rounded-[0.8rem] py-[0.7rem] px-[1.2rem] bg-gradient-to-b from-purple-400 via-purple-700 to-purple-800 font-semibold text-xl mt-6 mb-20"
				>Download CV</button
			>
		</a>
	</div>
	<div class="md:flex hidden">
		<img src={personagem} alt="imagem hero" />
	</div>
</section>

<section id="sobre" class="flex w-full h-[40rem] bg-tertiary-500 py-[1.5rem] px-[8rem]">
	<img class="hidden md:flex rounded-2xl" src={my_image} alt="minha foto" />

	<div class="flex flex-col pl-[3rem]">
		<h1 class="text-4xl font-semibold pb-[1rem]">Sobre mim</h1>

		<p class="text-lg">
			Sou Lari, uma desenvolvedora de software e apaixonada por tecnologia. Atualmente, curso
			Engenharia de Software na UNIVATES, me dedico não apenas em aprimorar minhas habilidades
			front-end, back-end e mobile, mas também explorar novas descobertas e conhecimentos. Minha
			jornada profissional começou como assistente de dados, onde tenho a oportunidade de explorar o
			mundo da análise de dados. Essa experiência despertou em mim uma paixão ainda maior por essa
			área, e agora busco me aprofundar no universo dos dados.
		</p>
		<div class="mt-[1.6rem]">
			<FiltroSobre />
		</div>
	</div>
</section>
<section id="portfolio">
	<div class="flex flex-col items-center font-semibold p-3">
		<h1 class="text-4xl font-semibold pt-[2rem]">Portfólio</h1>
		<h3>Meus Projetos Recentes</h3>
	</div>
	<div class="flex justify-center pb-[4rem]">
		<Filtro_portfolio />
	</div>
</section>
