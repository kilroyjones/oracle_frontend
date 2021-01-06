<script>
  import Holding from "./Holding.svelte";
  import HoldingTableHeader from "./HoldingTableHeader.svelte";
  let holdings = "";

  async function getHoldings() {
    await fetch(`http://localhost:5000/holdings`)
      .then((r) => r.json())
      .then((data) => {
        holdings = data.slice(0, 10);
      });
  }
  getHoldings();
</script>

<style>
  .title {
    font-size: 16px;
    font-weight: bold;
    margin-bottom: 10px;
  }
</style>

<div class="columns">
  <div class="container">
    <div class="columns">
      <div class="title">The Oracle's Holdings</div>
    </div>
    <HoldingTableHeader />
    {#each holdings as holding}
      <Holding {holding} />
    {/each}
  </div>
</div>
