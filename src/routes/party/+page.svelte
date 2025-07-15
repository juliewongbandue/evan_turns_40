<script>
  import Button from '../../lib/button.svelte';
</script>

<article class="content">
<div class='body'>
  <h1>The Party</h1>
  <h2>Saturday, September 13, 2025</h2>
  <div class="flexRow">
    <p class="address">Pete's Candy Store
      <a href="https://maps.app.goo.gl/EADCaoEZ2Uy4Up6o7" target="_blank"><br/>
      709 Lorimer St
      <br/>
      Brooklyn, NY 11211</a>
    </p>
    <Button href='/rsvp'>RSVP</Button>
  </div>
  <div class="map-container">
  <iframe
    width="330"
    height="265"
    frameborder="0"
    style="border:0"
    referrerpolicy="no-referrer-when-downgrade"
    src="https://www.google.com/maps?q=Pete's+Candy+Store,+Brooklyn,+NY&z=17&output=embed"
    allowfullscreen>
  </iframe>
  </div>

  <p class='info'>Here's the loose timing of everything: </p>
  <ul>
    <li class="info"><b>2PM</b> - Arrive / make final outfit tweaks</li>
    <li class="info"><b>2:30PM-6PM</b> - Drinks, music, dancing, talk about me, or how much you're actually there for Julie.</li>
    <li class="info"><b>6:30PM</b> - The bar opens to regular service. You don't have to leave, but I will be going to dinner. I suggest you do the same!</li>
  </ul>
  <p class="info">
    <b>Dress code:</b> I want to see you in your New York best. Whatever
    that means to you.
  </p>
    <p class="info">
    <b>Vibe:</b> Pete's is very casual, laid back. There will be outdoor space.
    There will be music, potentially loud in one of the rooms. There will be drinks
    and some snacks and lots of funny and sweet people. Children are welcome, but
    I'm not sure they'll have a great time. Dogs are not allowed, which is a bummer.
    Feel free to stop by for a few or hang out the whole time!
  </p>
</div>
<div class="body">
  <h2>The After Party</h2>
  <p class='info'>
    After a break for dinner, I'll be posting up somewhere in Greenpoint/Williamsburg
    for the rest of the night. Details to come.
  </p>
</div>

<!-- ///// -->
<div class="body" style="margin-top: var(--space-5)">
  <h1>Early Birds</h1>
  <h2>Friday, September 12th, 2025</h2>
  <p class='info'>
    If you're in town on Friday and want to start celebrating early, I will almost definitely
    be doing improv at Magnet Theater with The Friday Night Sh*w. 9pm!
  </p>
</div>

<div class="body">
  <h1>Sickos Only</h1>
  <h2>Sunday, September 14th, 2025</h2>
  <p class='info'>
    If you're an absolute psycho and like punk music, I will be going to see NY legend Jeff
    Rosenstock and the bad boys of Ontario, PUP, at Brooklyn Paramount. <a href="https://www.ticketmaster.com/event/000062750A608011?irgwc=1&clickid=UAS15K1aYxycUaxUoESJU196UksSBeW5Ly4O180&camefrom=CFC_BUYAT_1387536&impradid=1387536&REFERRAL_ID=tmfeedbuyat1387536&wt.mc_id=aff_BUYAT_1387536&utm_source=1387536-Seated&impradname=Seated&utm_medium=affiliate&ircid=4272" target="_blank">Grab a ticket</a>, scream your head off, and ring in
    my actual birthday with me at midnight.
  </p>
  <div class="body">
  <h1>Birthday</h1>
  <h2>Monday, September 15th, 2025</h2>
  <p class='info'>
    I will be taking my actual birthday off from work. If you're around, lmk.
  </p>
</div>
  <img src="assets/pup-jeff-killian-young.jpg" width="100%" title="jeff rosenstock holds a microphone on stage while pup lead singer stefan babcock crowdsurfs over the excited masses at st. vitus. somewhere below stefan is evan. also visible is kind human pat cartelli. photo by killian young." alt="jeff rosenstock holds a microphone on stage while pup lead singer stefan babcock crowdsurfs over the excited masses at st. vitus. photo by killian young."/>
  <p class="more">Please email me with any questions at <a class='email' href="mailto:evanfortybarden@gmail.com?subject=Party Question">evanfortybarden at gmail</a>.</p>
</div>
</article>

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

.flexRow {
   display: flex;
   align-items: center;
   gap: var(--space-4);
}

</style>
