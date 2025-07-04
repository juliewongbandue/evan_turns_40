<script lang="ts">
  import { page } from '$app/state';
  import { browser } from '$app/environment';
  import {fade} from 'svelte/transition'
  export let data
</script>

<div class="wrapper">
<nav>
  <a href='/' class="hover-underline-animation">Home</a>
  <a href='/party' class="hover-underline-animation">Party</a>
  <a href='/rsvp' class="hover-underline-animation">RSVP</a>
  <a href='/fomo' class="hover-underline-animation">FOMO</a>
</nav>
<main transition:fade>
  {#key page.url}
  <div 
    in:fade={{ duration: 500 }}
    out:fade={{ duration: 50}}>
	<slot />
  </div>
  {/key}
</main>

<footer>
	Made with <span>&hearts;</span> by his favorite girlfriend &copy;2025
</footer>
</div>

<style>
  html, body {
  overflow-x: hidden;
  }
  .wrapper {
    min-height: 100%;
    display: grid;
    grid-template-rows: auto 1fr auto;
  }
	nav {
		padding: var(--space-3) var(--space-4);
		transition: var(--transition);
		border-bottom: var(--border-divider);
		display: flex;
		align-items: center;
		gap: var(--space-3);
		font-size: var(--font-size-3);
		font-family: var(--font-family-mono);
    background-color: var(--nav-background);
    text-align: center;
    position: sticky;
    top: 0;
    z-index: 1;
	}
  nav a {
    text-decoration: none;
    color: var(--gray-11);
    font-weight: 500;
    display: block;
    font-size: var(--font-size-2);
    font-family: var(--font-family-body);
  }

  @media (min-width:320px)  { 
    /* smartphones, iPhone, portrait 480x320 phones */
    nav a {
      font-size: var(--font-size-3);
      display: block;
    }
  }
  .hover-underline-animation {
    display: inline-block;
    position: relative;
    border-radius: 3px;
  }

.hover-underline-animation::after {
  content: '';
  position: absolute;
  width: 100%;
  transform: scaleX(0);
  height: 2px;
  bottom: 0;
  left: 0;
  background-color: var(--blue-9);
  transform-origin: bottom right;
  transition: transform 0.25s ease-out;
}

.hover-underline-animation:hover::after {
  transform: scaleX(1);
  transform-origin: bottom left;
}

.hover-underline-animation:focus-visible {
  outline: 2px solid var(--gray-6);
  outline-offset: 2px;
}

.hover-underline-animation:focus-visible::after {
  transform: scaleX(1);
  transform-origin: bottom left;
}

	footer {
		color: var(--gray-4);
		font-family: var(--font-family-mono);
		font-size: 0.5rem;
		padding: var(--space-2) var(--space-4);
    letter-spacing: var(--letter-spacing-tracked);
	}
	footer span {
		color: var(--red-7);
	}
</style>
