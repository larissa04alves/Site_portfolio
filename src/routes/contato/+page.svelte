<script>
	import cellphone from '$lib/assets/img/cellphone.svg';
	import email from '$lib/assets/img/email.svg';
	import git_contato from '$lib/assets/img/git_contato.svg';
</script>

<section class="flex justify-evenly items-center mt-[8rem]">
	<div class="flex flex-col items-center">
		<img class="w-16" src={cellphone} alt="icon" />
		<h1 class="font-semibold text-xl">Telefone</h1>
		<a
			target="_blank"
			href="https://api.whatsapp.com/send/?phone=5596913627&text&type=phone_number&app_absent=0"
		>
			<p class="text-lg">(55) 99691-3627</p>
		</a>
	</div>
	<div class="flex flex-col items-center">
		<img class="w-16" src={email} alt="icon" />
		<h1 class="font-semibold text-xl">Email</h1>
		<p class="text-lg">alves04.larissa@gmail.com</p>
	</div>
	<div class="flex flex-col items-center">
		<img class="w-16" src={git_contato} alt="icon" />
		<h1 class="font-semibold text-xl">GitHub</h1>
		<a target="_blank" href="https://github.com/larissa04alves">
			<p class="text-lg">@larissa04alves</p>
		</a>
	</div>
</section>

<div class="flex flex-col mt-[5rem] items-center">
	<label class="flex flex-col">
		<h1 class="flex flex-col text-4xl font-bold text-secondary-400">Entre em Contato</h1>
		<div class=" flex mt-8 w-[65rem] gap-4">
			<input class="input" type="text" placeholder="Nome" />
			<input class="input" type="text" placeholder="Email" />
		</div>

		<div class="flex mt-4 w-[65rem]">
			<input class="input" type="text" placeholder="Assunto" />
		</div>
	</label>
	<label class="flex w-[65rem] mt-4">
		<textarea class="textarea" rows="3" placeholder="Sua mensagem" />
	</label>
	<button
		class="rounded-[0.8rem] py-[0.6rem] px-[1.3rem] bg-gradient-to-b from-purple-500 via-purple-600 to-purple-700 font-semibold text-xl mt-6 mb-20"
		>Enviar email</button
	>
</div>
