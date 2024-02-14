<script>
	import logo from '$lib/assets/img/logo.svg';
</script>

<header class="geral">
	<a href="#">
		<img class="logo" src={logo} alt="Logo" />
	</a>
	<nav class="links">
		<a class="animado" href="#1">Home</a>
		<a class="animado" href="#2">Sobre</a>
		<a class="animado" href="#">Portfólio</a>
	</nav>
	<a href="#">
		<button class="btn"> Contato </button>
	</a>
</header>

<style>
	.geral {
		position: fixed;
		box-shadow: 0px 0px 8px #3f1397;
		background-color: #151515;
		width: 100%;
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding: 5px 70px 5px 70px;
		z-index: 100;
	}

	.logo {
		width: 150px;
	}

	.links {
		display: flex;
		gap: 60px;
		font-weight: 600;
		font-size: 16px;
	}

	.animado {
		position: relative;
		text-decoration: none;
	}
	.animado::before {
		content: '';
		position: absolute;
		width: 100%;
		height: 4px;
		border-radius: 2px;
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

	.btn {
		border: 1px solid #a666ff;
		border-radius: 12px;
		padding: 5px 25px;
		color: #e1cdfe;
		font-weight: 600;
	}

	.btn:hover {
		background-color: #3f1397;
		border: 1px solid #3f1397;
	}
</style>
