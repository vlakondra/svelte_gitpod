<script>
	import Comp1 from './Comps/comp1.svelte'
	import Comp2 from './Comps/comp2.svelte'
	let cmp =true;
</script>

<div class="main">
	<div>
		<button on:click={()=>cmp=!cmp}>Переключатель</button>
	</div>
	<div>
		{#if cmp}
		<Comp1 text='Первый'/>
		{:else}
		<Comp2 text='Второй'/>
		{/if}
		
	</div>
</div>

<style>
	.main {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		min-height:100%;
	}
</style>
