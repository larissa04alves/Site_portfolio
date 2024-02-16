<script>
	let isChecked = false;

	function toggleCheckbox() {
		isChecked = !isChecked;
	}
</script>

<section>
	<div
		class={isChecked ? 'toggle-container checked' : 'toggle-container'}
		on:click={toggleCheckbox}
	>
		<div id="bar1" class="bars"></div>
		<div id="bar2" class="bars"></div>
		<div id="bar3" class="bars"></div>
	</div>
</section>

<style>
	.toggle-container {
		position: relative;
		width: 2rem;
		height: 2rem;
		cursor: pointer;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		transition-duration: 0.5s;
		gap: 0.5rem;
	}

	.bars {
		width: 100%;
		height: 0.1rem;
		background-color: rgb(92, 130, 255);
		border-radius: 0.5rem;
		transition-duration: 0.5s;
	}

	.toggle-container.checked #bar2 {
		transform: scaleX(0);
	}

	.toggle-container.checked #bar1 {
		transform: rotate(45deg);
	}

	.toggle-container.checked #bar3 {
		transform: rotate(-45deg);
	}

	.toggle-container.checked {
		transform: rotate(180deg);
	}
</style>
