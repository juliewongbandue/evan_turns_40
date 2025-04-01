<script lang="ts">
	import { page } from '$app/state';
	import { browser } from '$app/environment';

	let darkMode: boolean;

	function handleSwitchDarkMode() {
		darkMode = !darkMode;

		darkMode
			? document.documentElement.setAttribute('data-theme', 'dark-mode')
			: document.documentElement.removeAttribute('data-theme');
	}

	if (browser) {
		if (window.matchMedia('(prefers-color-scheme: dark)').matches) {
			document.documentElement.setAttribute('data-theme', 'dark-mode');
			darkMode = true;
		} else {
			document.documentElement.removeAttribute('data-theme');
			darkMode = false;
		}
	}
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
		position: absolute;
		bottom: 0;
	}

	footer span {
		color: var(--red-7);
	}

	label {
		display: flex;
		align-items: center;
		gap: var(--space-2);
		cursor: pointer;
	}

	.toggleContainer {
		position: relative;
		width: var(--toggleContainer-width);
		height: var(--toggleContainer-height);
	}

	.toggleContainer input {
		outline: none;
		height: 1;
		width: 1;
	}

	.toggle {
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		background-color: var(--primary);
		border-radius: var(--border-radius-4);
	}

	.toggle::before,
	.toggle::after {
		--toggle-size: 20px;
		position: absolute;
		content: '';
		height: var(--toggle-size);
		width: var(--toggle-size);
		left: var(--space-1);
		bottom: var(--space-1);
		background-color: var(--toggle-color, var(--gray-11));
		transition: var(--duration-1);
		border-radius: 50%;
	}

	input:checked + .toggle::before {
		transform: translateX(23px);
		background-color: var(--background);
	}

	input:checked + .toggle::after {
		transform: translate(15px);
		background-color: var(--checked-color, var(--primary));
	}

	.toggle-input::after {
		opacity: 0;
		border: var(--focus);
		content: '';
		display: block;
		height: var(--toggleContainer-height);
		width: var(--toggleContainer-width);
		border-radius: var(--border-radius-4);
		top: -6px;
		left: -6px;
		position: absolute;
		transition: var(--transition);
	}

	.toggle-input:focus::after {
		opacity: 1;
		padding: var(--space-1);
	}
</style>
