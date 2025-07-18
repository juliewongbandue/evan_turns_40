<script>
  export let open = false;
	import { slide } from 'svelte/transition';
	const handleClick = () => open = !open
</script>

<div class="accordion">
	<div class="header" on:click={handleClick}>
    <button class="accordion-button" class:accordion-open={open}/>
		<div class="text">
			<slot name="head"></slot>
		</div>


	</div>

	{#if open}
	<div class="details" transition:slide>
		<slot name="details">
		</slot>
	</div>
	{/if}
</div>

<style>
	div.accordion {
		margin: 1rem 0;
	}

	div.header {
		display:flex;
    gap: var(--space-2);
    background-color: var(--orange-9);
    padding: var(--space-2);
		align-items: center;
	}

	div.header .text {
		flex: 1;
		margin-right: 5px;
	}

	div.details {
		background-color: var(--blue-10);
		padding: var(--space-1);
	}

   p.content {
		margin: 0;
	}

  .accordion-button {
    height: 1rem;
		width: 1rem;
		background-image: url('/assets/right-thin-chevron.png');
		background-size: contain;
		border: none;
		transition: transform .2s ease-in-out;
		background-color: transparent;
		border-radius: 3px;
  }

	.accordion-button:focus-visible{
		outline: 2px solid var(--blue-10);
 		outline-offset: 2px;
	}

	.accordion-open {
		transform: rotate(90deg);
	}

</style>
