<script>
  let currentIndex = 0;

	let images = Array.from({length: 28}).map((image, i) => `/assets/${i + 1}.jpeg`)

  function goToNext() {
    currentIndex = (currentIndex + 1) % images.length;
  }

  function goToPrevious() {
    currentIndex = (currentIndex - 1 + images.length) % images.length;
  }

</script>

<style>
  .carousel {
    position: relative;
    width: 100%;
    max-width: 600px;
    margin: auto;
    overflow: hidden;
  }

  .carousel-images {
    display: flex;
    transition: transform 0.5s ease-in-out;
  }

  .carousel-images img {
    width: 100%;
    max-width: 100%;
    display: block;
  }

  .button {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background: rgba(0, 0, 0, 0.5);
    color: white;
    border: none;
    padding: 10px;
    cursor: pointer;
    font-size: 18px;
  }

  .prev {
    left: 10px;
  }

  .next {
    right: 10px;
  }
</style>

<div class="carousel">
  <div class="carousel-images" style="transform: translateX(-{currentIndex * 100}%)">
    {#each images as image}
      <img src={image} alt="carousel image" />
    {/each}
  </div>

  <button class="button prev" on:click={goToPrevious}>&lt;</button>
  <button class="button next" on:click={goToNext}>&gt;</button>
</div>
