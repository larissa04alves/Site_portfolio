<script>
	import { dataPortfolio } from '$lib/assets/data/dataPortfolio';

	import portfolio from '$lib/assets/img/portfolio.svg';
</script>

{#each dataPortfolio.Projeto4 as projeto4}
	<div class="card-container">
		<a target="_blank" href="https://portfolio-nine-eta-92.vercel.app/">
			<div class="card w-full h-full">
				<img src={portfolio} alt="image" />
				<div class="front-content">
					<h1 class="text-xl font-semibold">{projeto4.title}</h1>
					<h2 class="text-xl">{projeto4.category}</h2>
				</div>
				<div class="content">
					<p class="heading">{projeto4.title_back}</p>
					<p>{projeto4.description}</p>
					<p class="font-semibold">{projeto4.tecnologias}</p>
				</div>
			</div>
		</a>
	</div>
{/each}

<style>
	.card-container {
		width: 28rem;
		height: 16rem;
		position: relative;
		border-radius: 1rem;
		box-shadow: 0 0.9rem 1.3rem rgba(0, 0, 0, 0.2);
		overflow: hidden;
	}

	.card {
		width: 100%;
		height: 100%;
		border-radius: inherit;
	}

	.card .front-content {
		display: flex;
		flex-direction: column;
		padding: 1rem 0 0 2rem;
		font-size: 1.5rem;
		font-weight: 600;
		transition: all 0.6s cubic-bezier(0.23, 1, 0.32, 1);
	}

	.card .front-content p {
		font-size: 3rem;
		font-weight: 700;
		opacity: 1;
		background: linear-gradient(-45deg, #9675eb 0%, #7a5a99 100%);
		background-clip: text;
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		transition: all 0.6s cubic-bezier(0.23, 1, 0.32, 1);
	}

	.card .content {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		text-align: center;
		gap: 10px;
		background: linear-gradient(-45deg, #4f1ad5 0%, #9540e6 100%);
		color: #e8e8e8;
		padding: 20px;
		line-height: 1.5;
		border-radius: 5px;
		pointer-events: none;
		transform: translateX(-96%);
		transition: all 0.6s cubic-bezier(0.23, 1, 0.32, 1);
	}

	.card .content .heading {
		font-size: 32px;
		font-weight: 700;
	}

	.card:hover .content {
		transform: translateY(0);
	}

	.card:hover .front-content {
		transform: translateX(-30%);
	}

	.card:hover .front-content p {
		opacity: 0;
	}
</style>
