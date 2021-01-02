<script>
	import Holding from "./Holding.svelte";
	import Navbar from "./Navbar.svelte";
	import News from "./News.svelte";
	import TickerBar from "./TickerBar.svelte";

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

<style>
	.full-width {
		padding: 0px;
		margin: 0px;
	}
	.news-container {
		background-color: black;
		padding: 0px;
	}
</style>

<div class="container full-width">
	<Navbar />
	<div class="container grid-xl">
		<div class="columns">
			<TickerBar />
		</div>
		<div class="columns">
			<div class="news-container column col-6">
				<News />
			</div>
			<div class="column col-3">Headlines</div>
			<div class="column col-3">
				{#each holdings as holding}
					<Holding {holding} />
				{/each}
			</div>
		</div>
	</div>
</div>
