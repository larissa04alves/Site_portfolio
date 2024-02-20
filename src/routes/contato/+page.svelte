<script>
	import cellphone from '$lib/assets/img/cellphone.svg';
	import email from '$lib/assets/img/email.svg';
	import git_contato from '$lib/assets/img/git_contato.svg';
</script>

<section class="infos">
	<div>
		<img class="w-16" src={cellphone} alt="icon" />
		<h1 class="font-semibold text-xl">Telefone</h1>
		<p class="text-lg">(55) 99691-3627</p>
	</div>
	<div>
		<img class="w-16" src={email} alt="icon" />
		<h1 class="font-semibold text-xl">Email</h1>
		<p class="text-lg">alves04.larissa@gmail.com</p>
	</div>
	<div>
		<img class="w-16" src={git_contato} alt="icon" />
		<h1 class="font-semibold text-xl">GitHub</h1>
		<p class="text-lg">@larissa04alves</p>
	</div>
</section>

<div class="contato">
	<label class="label">
		<h1 class="text-3xl font-bold text-secondary-400">Entre em Contato</h1>
		<div class="">
			<input class="input" type="text" placeholder="Nome" />
			<input class="input" type="text" placeholder="Email" />
		</div>

		<div class="assunto">
			<input class="input" type="text" placeholder="Assunto" />
		</div>
	</label>
	<label class="label">
		<textarea class="textarea" rows="3" placeholder="Sua mensagem" />
	</label>
</div>

<style>
	.infos {
		display: flex;
		justify-content: space-evenly;
		align-items: center;
		margin-top: 9rem;
	}
	.contato {
		display: flex;
		flex-direction: column;

		margin-top: 2rem;
	}

	.label {
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.input {
		width: 30rem;
		height: 2.8rem;
		border: 0.15rem solid #a666ff;
		border-radius: 0.7rem;
		margin-top: 2rem;
	}

	.textarea {
		width: 60rem;
		height: 10rem;
		border: 0.13rem solid #a666ff;
		border-radius: 0.7rem;
		margin-top: 2rem;
	}
</style>
