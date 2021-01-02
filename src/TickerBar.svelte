<!-- https://css-tricks.com/can-get-pretty-far-making-slider-just-html-css/ -->
<script>
  import TickerBarElement from "./TickerBarElement.svelte";

  let tickers = [
    { ticker: "TSLA", price: 560.32, change: 25.03 },
    { ticker: "BTC", price: 98.32, change: 2.03 },
    { ticker: "PLTR", price: 5.32, change: -1.34 },
    { ticker: "AAPL", price: 170.01, change: -1.34 },
    { ticker: "GOLD", price: 88.18, change: 10.34 },
    { ticker: "GOLD", price: 88.18, change: -20.34 },
    { ticker: "GOLD", price: 88.18, change: 10.34 },
    { ticker: "GOLD", price: 88.18, change: 10.34 },
    { ticker: "GOLD", price: 88.18, change: -10.34 },
    { ticker: "GOLD", price: 88.18, change: 10.34 },
    { ticker: "GOLD", price: 88.18, change: 10.34 },
  ];
</script>

<style>
  .scrolling-wrapper-flexbox {
    display: flex;
    flex-wrap: nowrap;
    overflow-x: auto;
  }

  .scrolling-wrapper,
  .scrolling-wrapper-flexbox {
    width: 100%;
    -webkit-overflow-scrolling: touch;
    scroll-snap-type: x mandatory;
  }
  ::-webkit-scrollbar {
    display: none;
  }
</style>

<div class="scrolling-wrapper">
  <div class="scrolling-wrapper-flexbox">
    {#each tickers as ticker}
      <TickerBarElement
        ticker={ticker.ticker}
        price={ticker.price}
        change={ticker.change} />
    {/each}
  </div>
</div>
