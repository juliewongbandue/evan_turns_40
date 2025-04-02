<script>
  let currentIndex = 0;
  let images = Array.from({length: 33}).map((_image, i) => `/assets/${i + 1}.jpeg`);

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
    max-width: 600px;
    overflow: hidden;
		height: 500px;
		display: block;
  }

  .carousel-images {
    display: flex;
    transition: transform 0.5s ease-in-out;
		height: 100%;
  }

  .carousel-images div {
    flex: 0 0 100%; /* Make sure each div takes 100% of the carousel width */
    height: 100%; /* Make sure they fill the container height */
    background-size: contain;
		background-repeat: no-repeat;
    background-position: center;
		border-radius: var(--border-radius-3);
  }

  .button {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background: rgba(0, 0, 0, 0.5);
    color: white;
    border: none;
    padding: var(--space-3);
    cursor: pointer;
    font-size: var(--font-size-5);
		border-radius: var(--border-radius-2)
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
    <img loading="lazy" alt='dad images'/>
      <div style="background-image: url({image})"></div>
    {/each}
  </div>

  <button class="button prev" on:click={goToPrevious}>&lt;</button>
  <button class="button next" on:click={goToNext}>&gt;</button>
</div>
