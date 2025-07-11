<script>
	import Button from '$lib/button.svelte';
</script>
<div class="content">
<h1>RSVP</h1>

<article class="body">
  <p>Please let me know if you'll be able to make it!</p>
  <p class="subText">(<a href="https://docs.google.com/forms/d/e/1FAIpQLScOZ-hOS_x63VWyxVd3q-u_wiOIRehrHA2vCOnbckDKmjqQ5g/viewform?usp=header" target="_blank">Click here</a> if you don't see a form below.)</p>

  <iframe src="https://docs.google.com/forms/d/e/1FAIpQLScOZ-hOS_x63VWyxVd3q-u_wiOIRehrHA2vCOnbckDKmjqQ5g/viewform?embedded=true" width="100%" height="1492" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>

<Button href="/fomo" style='padding-top: var(--space-4)'>I have fomo :(</Button>
</article>

</div>

<style>
  .subText {
  font-size: var(--font-size-0);
}
</style>
