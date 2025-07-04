<script>
import RSVPButton from '../lib/rsvpButton.svelte';
</script>


<article class='body'>

<div class="header-wrapper">
  <div class="text-reveal-container"></div>
  <svg viewBox="0 0 200 100vw" width="100%" height="auto">
    <mask id="text-mask" maskUnits="userSpaceOnUse" maskContentUnits="userSpaceOnUse"  width="100vw" height="200">
      <rect width="100vw" height="200" fill="white"/>
      <text x="10" y="100" font-family="var(--font-family-heading)" font-size="3rem" font-weight="normal" text-anchor="start">
        <tspan dy="0">Evan's</tspan>
      </text>
      <text x="10" y="150" font-family="var(--font-family-heading)" font-size="3rem" font-weight="normal" text-anchor="start">
        <tspan d="0">40th Birthday</tspan>
      </text>
    </mask>
  </svg>
</div>

  <div class="wiper-box"></div>

  <section class='content'>
  <section class='article-small'>

  <div>
    <h2>Saturday, September 13, 2025</h2>
    <div class='info'>
      <p><b>Pete's Candy Store</b>
        <br/>
        709 Lorimer Street
        <br/>
        Brooklyn, NY 11211
        <br/>
        2:00PM-6:00PM
      </p>
      <RSVPButton/>
    </div>
  </div>

  </section>
  <div class="image-wrapper" style="--image-border-color: var(--orange-1)">
    <div class='image-container'></div>
    <p class='image-description'>Some text about the photo</p>
  </div>

  <div class="image-wrapper" style="--image-border-color: var(--blue-9)">
    <p class='image-description'>Some text about the photo</p>
    <div class='image-container'></div>
  </div>

  <div class="image-wrapper">
    <div class='image-container'></div>
    <p class='image-description'>Some text about the photo</p>
  </div>


  <div class="image-wrapper" style="--image-border-color: var(--orange-8)">
    <p class='image-description'>Hope to catch you there!</p>
    <div class='image-container' style="background-image: url('assets/evan-1.jpeg'); background-position: bottom -486px right -100px;"></div>
  </div>

  <RSVPButton/>

  </section>
</article>

<style>
  .content {
    padding: var(--space-3)
  }

  .info {
    display: flex;
    gap: var(--space-4);
    align-content: center;
    align-items: center;
    flex-wrap: wrap;
    padding-bottom: var(--space-4);
  }
  .image-container {
    --image-size: 350px;
    height: var(--image-size);
    min-width: var(--image-size);
    max-width: var(--image-size);
    border-radius: 100%;
    background-color: var(--gray-2);
    border: 10px solid;
    border-color: var(--image-border-color, var(--blue-3));
    grid-area: var(--grid-column);
  }

  .image-wrapper {
    display: grid;
    max-width: 700px;
    gap: var(--space-3);
    align-items: center;
    grid-template-columns: repeat(2);
    grid-template-rows: auto;
    grid-template-areas: "one two";
  }

  .image-description {
    grid-area: var(--grid-area);
    text-wrap: wrap
  }

  /* Media Query for Mobile Devices */
@media (max-width: 767px) { 
  .info {
    gap: var(--space-3);
  }
  .image-wrapper {
    text-align: center;
    gap: 0;
    margin-bottom: var(--space-4);
    grid-template-columns: 1fr; 
    grid-template-areas: 
      "one"
      "two";
  }

  .image-container {
    --grid-area: one;
    --image-size: 300px;
    margin: auto;
  }

  .image-description {
    --grid-area: two;
   }
}

  .header-wrapper {
    position: sticky;
    z-index: 2;
    top: 86px;
  }

  .signature {
    font-family: var(--font-family-body);
    font-style: italic;
    color: var(--gray-4);
    font-size: var(--font-size-3);
    padding-top: var(--space-4);
  }

  .text-reveal-container {
    position: relative; 
    width: 100vw; 
    height: 200px; 
    backdrop-filter: blur(5px) invert(10%);
    /* blue-5 */
    background-color:rgba(0, 64, 110, 0.9); 
    -webkit-mask: url(#text-mask);
    mask: url(#text-mask);
    overflow: hidden;
  }
  
  .wiper-box {
    position: absolute;
    top: 86px;
    width: 100vw; 
    height: 200px;
    background-color: var(--orange-8); 
    animation: wipe-animation .5s ease-out;
    background-size: 75px 75px; 
  }

  @keyframes wipe-animation {
    0% { top: -200px } 
    100% { top: 86px }
  }

  svg {
    position: absolute;
    width: 0;
    height: 0;
    overflow: hidden;
  }
</style>
