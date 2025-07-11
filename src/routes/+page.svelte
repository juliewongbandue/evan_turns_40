<script>
import Button from '../lib/button.svelte';
</script>

<div class="header-wrapper">
  <div class="text-reveal-container"></div>
  <svg viewBox="0 0 200 100vw" width="100%" height="auto">
    <mask id="text-mask" maskUnits="userSpaceOnUse" maskContentUnits="userSpaceOnUse"  width="100vw" height="200">
      <rect width="100vw" height="200" fill="white"/>
      <text x="10" y="100" font-family="var(--font-family-heading)" font-size="var(--hero-text-size, 3.5rem)" font-weight="normal" text-anchor="start">
        <tspan dy="0">Evan's</tspan>
      </text>
      <text x="10" y="150" font-family="var(--font-family-heading)" font-size="var(--hero-text-size, 3.5rem)" font-weight="normal" text-anchor="start">
        <tspan d="0">40th Birthday</tspan>
      </text>
    </mask>
  </svg>
</div>
<div class="wiper-box"></div>

<article class='body'>

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
      <Button href='/rsvp'>RSVP</Button>
    </div>
  </div>

  </section>
  <div class="image-wrapper" style="--image-border-color: var(--orange-1)">
    <div class='image-container' style="background-image: url('assets/evan-2.jpg'); background-size: cover; background-repeat: no-repeat; background-position: 0px -60px"></div>
    <p class='image-description'>
      It's true. I have now spent four decades slithering around on this big rock called earth.
      I've also spent 15 glorious/delusional years in NYC.
      To celebrate both, I'm having a big party with a heafty bar minimum which I will need YOUR help getting through.
      There will be music, laughter, and high fives.
    </p>
  </div>

  <div class="image-wrapper" style="--image-border-color: var(--blue-9)">
    <p class='image-description'>
      Like many 40-year-olds, I was once a very cute child. Illegally cute.
      Then came self-awareness, puberty, an understanding of global injustices, and hair loss.
      Not necessarily in that order.
      I've got a few more years to go and it would be nice to kick them off good company.
    </p>
    <div class='image-container' style="background-image: url('assets/evan-tball.jpg'); background-size: 170%; background-repeat: no-repeat; background-position: -140px -160px"></div>
  </div>

  <div class="image-wrapper">
    <div class='image-container' style="background-image: url('assets/evan-power-joker.jpg'); background-size: 200%; background-repeat: no-repeat; background-position: -180px -60px"></div>
    <p class='image-description'>
      If you're thinking, <em>"This seems kind of overkill for a birthday party,"</em> you're right.
      But! it doesn't look like Julie and I are having a big wedding anytime soon,
      so when else is this gonna happen? Let's party.
      If you don't live near NYC, consider this your excuse to visit, or at least check out the <a href='/fomo'>FOMO</a> page.
    </p>
  </div>


  <div class="image-wrapper" style="--image-border-color: var(--orange-8); text-align: center;">
    <div class='image-description'>
      <p>Hope to catch you there!</p>
      <Button style="margin-top: var(--space-4); justify-self: center;" href='/rsvp'>RSVP</Button>
    </div>
    <div class='image-container' style="background-image: url('assets/evan-1.jpeg'); background-position: bottom -486px right -100px;"></div>
  </div>

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
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: auto;
    grid-template-areas: "one two";
  }

  .image-description {
    grid-area: var(--grid-area);
    text-wrap: wrap
  }

  .header-wrapper {
    position: sticky;
    z-index: 2;
    top: 86px;
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
    animation: bounce 1s ease-in-out;
  }

  @keyframes bounce {
    0% {
        transform: translateY(0);
    }
    20% {
        transform: translateY(-200px); /* First big jump */
    }
    40% {
        transform: translateY(0);
    }
    60% {
        transform: translateY(-100px); /* Second, smaller jump */
    }
    75% {
        transform: translateY(0);
    }
    85% {
        transform: translateY(-40px); /* Third, even smaller jump */
    }
    90% {
        transform: translateY(0);
    }
    95% {
        transform: translateY(-15px); /* Final tiny bounce */
    }
    100% {
        transform: translateY(0);
    }
  }

  svg {
    position: absolute;
    width: 0;
    height: 0;
    overflow: hidden;
  }

  @media (max-width: 390px) {
    .header-wrapper {
      --hero-text-size: 3rem;
    }
  }
  /* Media Query for Mobile Devices */
  @media (max-width: 767px) {
    .info {
      gap: var(--space-3);
    }

    .image-wrapper {
      text-align: center;
      gap: 0;
      margin-bottom: var(--space-5);
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
</style>
