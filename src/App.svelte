<script>
	import Holdings from "./Holdings.svelte";
	import Navbar from "./Navbar.svelte";
	import News from "./News.svelte";
	import TickerBar from "./TickerBar.svelte";
</script>

<style>
	.full-width {
		padding: 0px;
		margin: 0px;
	}
	#ticker-bar {
		margin-bottom: 20px;
	}
</style>

<div class="container full-width">
	<Navbar />
	<div class="container grid-xl">
		<div id="ticker-bar" class="columns">
			<TickerBar />
		</div>

		<div class="columns">
			<div class="column col-6">
				<News />
			</div>
			<div class="column col-3">Headlines</div>
			<div class="column col-3">
				<Holdings />
			</div>
		</div>
	</div>
</div>
