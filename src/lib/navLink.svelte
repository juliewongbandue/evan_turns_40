<script >
  let { href } = $props();
  import { page } from '$app/state';
</script>

  <a href={href} class="hover-underline-animation navLink" data-active={page.url.pathname === href}>
      <slot></slot>
  </a>

<style>

.navLink {
  text-decoration: none;
  color: var(--gray-11);
  font-weight: 500;
  display: block;
  font-size: var(--font-size-2);
  font-family: var(--font-family-body);
}

.navLink:focus-visible {
  outline: 2px solid var(--blue-10);
  outline-offset: 2px;
}

@media (min-width:320px)  {
  /* smartphones, iPhone, portrait 480x320 phones */
  .hover-underline-animation {
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
  background-color: var(--orange-7);
  transform-origin: bottom right;
  transition: transform 0.25s ease-out;
}

.hover-underline-animation:hover::after {
  transform: scaleX(1);
  transform-origin: bottom left;
}

.hover-underline-animation[data-active="true"]::after {
  transform: scaleX(1);
  transform-origin: bottom left;
}

a:focus-visible {
  outline: 2px solid var(--blue-10);
  outline-offset: 2px;
}

.hover-underline-animation:focus-visible::after {
  transform: scaleX(1);
  transform-origin: bottom left;
}
</style>