<script>
	import Comp1 from "./Comps/comp1.svelte";
	import Comp2 from "./Comps/comp2.svelte";
	let cmp = true;
	let count = 0;

	function toggle() {
		cmp = !cmp;
	}
	const funccount = () => {
		count++;
	};
</script>

<div class="main">
	<div>
		
		<button on:click={toggle}>Переключатель</button>
	</div>
	<div>
		{#if cmp}
			<Comp1 text="Первый" {funccount} />
		{:else}
			<Comp2 text="Второй" cnt={count} />
		{/if}
	</div>
</div>

<style>
	.main {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		min-height: 100%;
		border: 2px solid blue;
	}
</style>
