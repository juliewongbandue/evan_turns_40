<script lang="ts">
  import { page } from '$app/state';
  import { browser } from '$app/environment';
  import {fade} from 'svelte/transition'
  import { NavLink } from '$lib'

</script>

<div class="wrapper">
<nav>
  <a href='/' ><img class="evan" src='/assets/Evan.png' aria-label="home" alt="evan-svg"/> </a>
  <NavLink href='/' >Home</NavLink>
  <NavLink href='/party'>Party</NavLink>
  <NavLink href='/rsvp' >RSVP</NavLink>
  <NavLink href='/fomo' >FOMO</NavLink>
  <NavLink href='/faq' >FAQ</NavLink>
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
  Executive produced by Nancy Seidman
  <br/>
  Made with <span>&hearts;</span> by his favorite girlfriend &copy;2025
</footer>
</div>

<style>
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

  .evan {
    height: 50px;
    width: auto;
  }

	footer {
		color: var(--gray-4);
		font-family: var(--font-family-mono);
		font-size: 0.5rem;
		padding: var(--space-2) var(--space-3);
    letter-spacing: var(--letter-spacing-tracked);
	}
	footer span {
		color: var(--red-7);
	}
</style>
