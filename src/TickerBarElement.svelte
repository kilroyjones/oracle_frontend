<script>
  export let ticker;
  export let price;
  export let change;
</script>

<style>
  .card {
    width: 200px;
    min-width: 200px;
    margin-right: 10px;
    border-width: 0px;
    height: 80px;
    min-height: 80px;
  }
  #ticker {
    font-size: 18px;
    font-weight: bold;
  }
  #price {
    font-size: 14px;
    color: green;
    font-weight: bold;
  }
  #change {
    font-size: 14px;
    font-weight: bold;
  }
  .change-positive {
    color: green;
  }
  .change-negative {
    color: red;
  }
  #graph-content {
    position: relative;
  }
  #graph {
    position: absolute;
    bottom: 0px;
  }
</style>

<div class="card">
  <div class="columns">
    <div class="column col-xs-6">
      <div class="column">
        <div id="ticker">{ticker}</div>
        <div id="price">{price}</div>
        {#if change > 0.0}
          <div id="change" class="change-positive">{change}</div>
        {:else}
          <div id="change" class="change-negative">{change}</div>
        {/if}
      </div>
    </div>
    <div id="graph-content" class="column col-xs-6">
      <img id="graph" src="static/images/stock.png" alt="filler" />
    </div>
  </div>
</div>
