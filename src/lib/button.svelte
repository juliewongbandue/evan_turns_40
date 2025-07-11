<script >
  let { style = '', href } = $props();
</script>

<div class='button-layout' style={style}>
    <a class="button" href={href}>
      <slot></slot>
    </a>
</div>

<style>
  .button {
  display: block; 
  font-family: var(--font-family-heading);
  font-size: 2rem;
  padding: var(--space-3) var(--space-4);
  width: max-content;
  border-radius: var(--border-radius-4);
  text-decoration: none;
  color: var(--orange-9);
  background-color: var(--blue-5);
  transition: all var(--duration-0) var(--easing-function-2);
  }

  .button:hover {
    background-color: var(--blue-10);
    color: var(--orange-5);
  }

  .button-layout {
    display: flex; 
    gap: var(--space-3);
    flex-direction: column;
  }
</style>