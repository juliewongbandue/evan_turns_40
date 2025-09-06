<script>
import Button from '../lib/button.svelte';
</script>

  <div class='header-wrapper'>
      <h1 class='header'>Evan's 40th Birthday</h1>
  </div>

<article class='body'>
  <section class='content'>

  <div>
    <h2>Saturday, September 13, 2025</h2>
    <div class='info'>
      <p><b>Pete's Candy Store</b>
        <a href="https://maps.app.goo.gl/EADCaoEZ2Uy4Up6o7" target="_blank">
        <br/>
        709 Lorimer St
        <br/>
        Brooklyn, NY 11211
        <br/>
        </a>
        2:00PM-6:30PM
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
      To celebrate both, I'm having a big party with a hefty bar minimum which I will need YOUR help getting through.
      There will be music, laughter, and high fives.
    </p>
  </div>

  <div class="image-wrapper" style="--image-border-color: var(--blue-9)">
    <p class='image-description'>
      Like many 40-year-olds, I was once a very cute child. Illegally cute.
      Then came self-awareness, puberty, an understanding of global injustices, and hair loss.
      Not necessarily in that order.
      I've got a few more years to go and it would be nice to kick them off with good company.
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

</article>

<style>
  @keyframes bounce {
    0%, 50%, 80%, 100% {transform: translateY(0);}
    20% { transform: translateY(-200px)}
    40% {transform: translateY(-50px);}
    60% {transform: translateY(-15px);}
  }

  .header-wrapper {
    background-color: var(--blue-4);
    padding: var(--space-4);
  }
  .header {
    max-width: 700px;
    margin: auto;
    color: var(--orange-8);
    font-style: unset;
    animation: bounce 1s ease-in-out;
  }

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
