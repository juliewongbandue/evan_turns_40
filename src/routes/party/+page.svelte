<script>
  import RSVPButton from '../../lib/rsvpButton.svelte';
</script>
<div class="content">
<h1>Party Info</h1>

<section class='article-small'>

<div class='body'>
  <h2>Saturday, September 13, 2025</h2>
  <p class="address">Pete's Candy Store
    <br/>
    709 Lorimer Street
    <br/>
    Brooklyn, NY 11211
  </p>

  <h2>Schedule</h2>
  <p class='info'>The timing below is a loose outline: </p>
  <ul>
    <li class="info"><b>2PM</b> - Arrive</li>
    <li class="info"><b>2:30PM-6PM</b> - Drinks, music, dancing, talk about Evan, or how much you're actually there for Julie.</li>
  </ul>
  <p class="more">Please email me with any questions at <a class='email' href="mailto:evanfortybarden@gmail.com?subject=Party Question">evanfortybarden@gmail.com</a>.</p>
</div>

<RSVPButton/>

</section>
</div>

<style>

.address {
  font-size: var(--font-size-2);
}

.info {
  font-size: var(--font-size-1);
}
.body > .more {
  color: var(--gray-4);
  font-size: var(--font-size-1);
}

</style>
