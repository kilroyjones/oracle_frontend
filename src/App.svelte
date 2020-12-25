<script>
	import Holding from "./Holding.svelte";
	let holdings = "";
	async function getHoldings() {
		await fetch(`http://localhost:5000/holdings`)
			.then((r) => r.json())
			.then((data) => {
				holdings = data;
			});
	}
	getHoldings();
</script>

<div class="container">
	<div class="columns">
		<div class="column col-md-4" />
		<div class="column col-md-4">Heading goes here</div>
		<div class="column col-md-4" />
	</div>
</div>

<div class="container">
	<div class="columns">
		<div class="column col-xs-4" />
		<div class="column col-xs-4">
			{#each holdings as holding}
				<Holding {holding} />
			{/each}
		</div>
		<div class="column col-xs-4" />
	</div>
</div>
