<script>
  export let holding;
  let gain = (
    parseFloat(holding.current_price) -
    parseFloat(holding.purchased_price - Math.random())
  ).toFixed(2);
  let percentage = (gain / parseFloat(holding.purchased_price)).toFixed(2);
</script>

<style>
  #ticker {
    width: 35%;
    min-width: 70px;
    color: #0f69ff;
    font-weight: bold;
  }
  #price {
    width: 20%;
    min-width: 50px;
    font-weight: bold;
    text-align: right;
  }
  #change {
    width: 20%;
    min-width: 50px;
    text-align: right;
  }
  #percentage {
    width: 20%;
    min-width: 50px;
    text-align: right;
  }
  #name {
    font-size: 10px;
    color: #888;
    margin-top: 1px;
  }
  #separator {
    border-bottom: 1px solid #eee;
    font-size: 12px;
    margin-bottom: 6px;
  }
  .columns {
    font-size: 14px;
  }
</style>

<div class="columns">
  <div id="ticker">{holding.ticker}</div>
  <div id="price">{holding.current_price}</div>
  <div id="change">{gain}</div>
  <div id="percentage">{percentage}</div>
</div>
<div id="separator" class="columns mb-2">
  <div id="name">{holding.name}</div>
</div>
