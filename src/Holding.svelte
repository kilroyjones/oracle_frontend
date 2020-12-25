<script>
  export let holding;
  let gain = holding.current_price - holding.purchased_price;
</script>

<style>
  .gain {
    font-size: 26px;
    font-weight: 700;
    color: green;
  }
  .loss {
    font-size: 12px;
    font-weight: 700;
    color: red;
  }
  .current-price {
    font-size: 14px;
  }
  .purchase-price {
    font-size: 12px;
  }
</style>

<div class="tile tile-centered">
  <div class="tile-content">
    <div class="tile-title">{holding.ticker}</div>
    <small class="tile-subtitle text-gray">Purchased:
      {holding.date_active}</small>
  </div>
  <div class="tile-action">
    <div class="current-price text-right">{holding.current_price}</div>
    <div class="purchase-price text-right">{holding.purchased_price}</div>
  </div>
  {#if { gain } < 0.0}
    <div class="pl-2 loss tile-action">{gain}</div>
  {:else}
    <div class="pl-2 gain tile-action">{gain}</div>
  {/if}
</div>
