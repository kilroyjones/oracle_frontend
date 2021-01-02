<script>
  import NewsCard from "./NewsCard.svelte";
  let news = [
    {
      image: "static/images/news/1.jpg",
      text:
        "Prices on lightbulbs surge with Tesla purchase of Edison's monocle",
    },
    {
      image: "static/images/news/2.jpg",
      text: "Money falls from the sky in latest Fed push to combat deflation",
    },
    {
      image: "static/images/news/3.jpg",
      text: "Grow weed from Bitcoin profits",
    },
  ];

  let imageIndex = 0;
  let imageLast = news.length - 1;
  setInterval(() => {
    if (imageIndex == imageLast) {
      imageIndex = 0;
    } else {
      imageIndex++;
    }
  }, 3000);
</script>

<style>
  .container {
    position: relative;
    margin: 0px;
    padding: 0px !important;
    height: auto;
  }
  /* img {
    opacity: 0;
    transition: opacity 0.5s;
  }
  .visible {
    opacity: 1;
  } */
</style>

<div class="container">
  <NewsCard image={news[imageIndex].image} title={news[imageIndex].text} />
</div>
