<script>
  export let holding;
  let gain = holding.current_price - holding.purchased_price;
</script>

<style>
  .tile-style {
    border-radius: 6px;
    background-color: #f95700ff;
    color: #eee;
    padding: 8px;
    width: 500px;
  }
  .price-heading {
    font-size: 18px;
    color: #eee;
  }
  .gain {
    font-weight: 700;
    color: #c9ffe7;
  }
  .loss {
    font-size: 12px;
    font-weight: 700;
    color: #ffbfc7;
  }
  .tile-title {
    font-size: 26px;
    color: #eee;
  }
</style>

<!-- <div class="mb-1 tile tile-centered tile-style">
  <div class="tile-content">
    <div class="text-bold tile-title">{holding.ticker}</div>
  </div>
  <div class="tile-action">
    <div class="price-heading text-bold text-right">Purchased</div>
    <div class="text-right text-bold">{holding.purchased_price}</div>
  </div>
  <div class="pl-2 tile-action">
    <div class="price-heading text-bold text-right">Current</div>
    <div class="text-right text-bold">{holding.purchased_price}</div>
  </div>
  <div class="pl-2 pr-2 tile-action" />

  <div class="pl-2 tile-action">
    <div class="price-heading text-bold text-right">Gain</div>
    <div class="text-right text-bold">
      {#if { gain } < 0.0}
        <div class="pl-2 loss tile-action">{gain}</div>
      {:else}
        <div class="pl-2 gain tile-action">{gain}</div>
      {/if}
    </div>
  </div>
</div> -->
