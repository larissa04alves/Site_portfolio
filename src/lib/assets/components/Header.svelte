<script lang="ts">
	import logo from '$lib/assets/img/logo.svg';
</script>

<header class="geral">
	<a href="/">
		<img class="logo" src={logo} alt="Logo" />
	</a>

	<nav class="links">
		<a class="animado" href="/" on:click={handleClick}>Home</a>
		<a class="animado" href="#sobre" on:click={handleClick}>Sobre</a>
		<a class="animado" href="#portfolio" on:click={handleClick}>Portfólio</a>
	</nav>
	<a href="/contato">
		<button class="btn"> Contato </button>
	</a>
</header>

<style>
	.geral {
		position: fixed;
		box-shadow: 0 0 0.5rem #3f1397;
		background-color: #151515;
		width: 100%;
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding: 0.3rem 4.3rem 0.3rem 4.3rem;
		z-index: 100;
	}

	.logo {
		width: 9.3rem;
	}

	.links {
		display: flex;
		gap: 3.75rem;
		font-weight: 600;
		font-size: 1rem;
	}

	.animado {
		position: relative;
		text-decoration: none;
	}
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

	.btn {
		border: 0.06rem solid #a666ff;
		border-radius: 0.8rem;
		padding: 0.3rem 1.6rem;
		color: #e1cdfe;
		font-weight: 600;
	}

	.btn:hover {
		background-color: #3f1397;
		border: 0.06rem solid #3f1397;
	}

	/* Media query for smaller devices */
	@media only screen and (max-width: 500px) {
		.geral {
			display: flex;
			justify-content: space-around;
		}

		.links {
			display: none;
			flex-direction: column;
			position: absolute;
			top: 4rem;
			width: 50%;
			background-color: #3f1397;
			box-shadow: 0 0 0.5rem #3f1397;
			z-index: 99;
		}
		.logo {
			display: none;
		}
	}
</style>
