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
    <p>This is some example content. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
    <p>More content to make the page scrollable.</p>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
    <p>Even more content to ensure ample scrolling space.</p>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
    
</article>

<style>
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
