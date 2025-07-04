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
  <div class="image-wrapper" style="--image-border-color: var(--orange-1)">
    <div class='image-container'></div>
    <p class='image-description'>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quis laborum sint provident facere harum hic illo eveniet assumenda expedita labore. Est nihil minima cupiditate laboriosam quisquam quidem, beatae totam accusamus!</p>
  </div>

  <div class="image-wrapper" style="--image-border-color: var(--blue-9)">
    <p class='image-description'>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quis laborum sint provident facere harum hic illo eveniet assumenda expedita labore. Est nihil minima cupiditate laboriosam quisquam quidem, beatae totam accusamus!</p>
    <div class='image-container'></div>
  </div>

  <div class="image-wrapper">
    <div class='image-container'></div>
    <p class='image-description'>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quis laborum sint provident facere harum hic illo eveniet assumenda expedita labore. Est nihil minima cupiditate laboriosam quisquam quidem, beatae totam accusamus!</p>
  </div>


  <div class="image-wrapper" style="--image-border-color: var(--orange-8)">
    <p class='image-description'>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quis laborum sint provident facere harum hic illo eveniet assumenda expedita labore. Est nihil minima cupiditate laboriosam quisquam quidem, beatae totam accusamus!</p>
    <div class='image-container'></div>
  </div>
  </section>
    
</article>

<style>
  .content {
    padding: var(--space-3)
  }
  .image-container {
    height: 200px;
    min-width: 200px;
    border-radius: 100%;
    background-color: var(--gray-2);
    border: 10px solid;
    border-color: var(--image-border-color, var(--blue-3));
  }

  .image-wrapper {
    display: flex;
    max-width: 700px;
    gap: var(--space-4);
    align-items: center;
  }

  .image-description {
    flex-grow: 1;
  }

  .header-wrapper {
    position: sticky;
    z-index: 2;
    top: 54px;
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
    /* backdrop-filter: blur(10px); */
    -webkit-mask: url(#text-mask);
    mask: url(#text-mask);
    overflow: hidden; 
  }
  
  .wiper-box {
    position: absolute;
    top: 54px;
    width: 100vw; 
    height: 200px;
    background-color: var(--orange-8); 
    animation: wipe-animation .5s ease-out;
  }

  @keyframes wipe-animation {
    0% { top: -200px } 
    100% { top: 54px }
  }

  svg {
    position: absolute;
    width: 0;
    height: 0;
    overflow: hidden;
  }
</style>
