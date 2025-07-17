<script>
  export let open = false;
	import { slide } from 'svelte/transition';
	const handleClick = () => open = !open
</script>

<div class="accordion">
	<div class="header" on:click={handleClick}>
    <button class="accordion-button">
    {#if open}
    ﹀
    {:else}
    〉
    {/if}
		</button>
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
		width:100%;
    gap: var(--space-2);
    background-color: var(--orange-9);
    padding: var(--space-2);
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
    /* padding-left: var(--space-2); */
    /* text-align: 'center'; */
  }
</style>
