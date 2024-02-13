<script>
	import logo from '$lib/assets/img/logo.svg';
</script>

<header class="geral">
	<a href="#">
		<img class="logo" src={logo} alt="Logo" />
	</a>
	<nav class="links animado">
		<a href="#">Home</a>
		<a href="#">Sobre</a>
		<a href="#">Portfólio</a>
	</nav>
	<a href="#">
		<button class="btn"> Contato </button>
	</a>
</header>

<style>
	.geral {
		display: flex;
		align-items: center;
		justify-content: space-between;
		margin: 10px 150px 0 150px;
	}

	.logo {
		width: 180px;
	}

	.links {
		display: flex;
		gap: 60px;
		font-weight: 500;
	}

	.animado {
		position: relative;
		text-decoration: none;
	}
	.animado::before {
		content: '';
		position: absolute;
		width: 100%;
		height: 2px;
		border-radius: 3px;
		background-color: #a666ff;
		bottom: 0;
		left: 0;
		transform-origin: right;
		transform: scaleX(0);
		transition: transform 0.3s ease-in-out;
	}
	.animado :hover::before {
		transform-origin: left;
		transform: scaleX(1);
	}

	.btn {
		border: 1px solid #a666ff;
		border-radius: 12px;
		padding: 6px 30px;
		color: #e1cdfe;
		font-weight: 600;
	}
</style>
