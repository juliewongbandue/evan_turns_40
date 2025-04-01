<script lang="ts">
	// import { page } from '$app/state';
	// import { browser } from '$app/environment';
</script>

<nav>
  <a href='/'>home</a>
  <a href='/memorial-info'>memorial info</a>
  <a href='/memories'>memories</a>
  <a href='/give'>give</a>
</nav>
<main>
	<slot />
</main>

<footer>
	<p>Made with <span>&hearts;</span> by his favorite daughter &copy;2025 </p>
</footer>

<style>
	main {
		padding: var(--space-4);
	}
	nav {
		padding: var(--space-3);
		transition: var(--transition);
		border-bottom: var(--border-divider);
		display: flex;
		justify-content: flex-end;
		align-items: center;
		gap: var(--space-2);
		font-size: var(--font-size-3);
		font-family: var(--font-family-mono);
		color: var(--primary);
	}
	footer {
		color: var(--primary);
		font-family: var(--font-family-mono);
		font-size: var(--font-size-1);
		padding: var(--space-2) var(--space-4);
	}

	footer span {
		color: var(--red-7);
	}
</style>
