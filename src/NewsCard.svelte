<script>
  import { fade } from "svelte/transition";
  export let image;
  export let title;
</script>

<style>
  .headline {
    position: absolute;
    bottom: 10px;
    left: 10px;
    font-size: 26px;
    color: #fff;
  }
  .image-sizing {
    width: 100%;
    height: auto;
  }
  img {
    opacity: 1;
    transition: opacity 0.5s;
  }
  .container {
    padding: 0px;
    height: auto;
  }
</style>

<div class="container">
  <img transition:fade class="image-sizing" src={image} alt={title} />
  <div class="headline">{title}</div>
</div>
