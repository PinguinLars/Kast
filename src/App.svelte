<script>
  let y;
  $: console.log(y);
</script>

<svelte:window bind:scrollY={y}/>

<div class="pre-transition">
  <h1>Hé, ik wil je iets vertellen</h1>
  <!-- Might comment this -->
  <sub>Maar, kan je dit niet door vertellen?</sub>
  <p>
    Ik vind dit best wel moeilijk om dit te vertellen, maar ik wil het wel vertellen.<br/>
    Scroll langzaam!
  </p>
  <p>Ik voel me:</p> <!-- why does it look sad? -->
</div>
<div class="transition">
  {#if y >= 40}
    <p>niet</p>
    <div class="white-strip vertical-strip">
    </div>
  {/if}
  {#if y >= 50}
    <p>echt</p>
    <div class="white-strip vertical-strip">
    </div>
  {/if}
  {#if y >= 60}
    <p>een</p>
    <div class="vertical-strip-box">
      <div class="white-strip vertical-strip">
      </div>
    </div>
  {/if}
  {#if y >= 70}
    <!--suppress GrazieInspection -->
    <p>jongen,</p>
    <div class="vertical-strip-box" id="first-blue-apparence">
      <div class="blue-strip vertical-strip">
      </div>
      <div class="white-strip vertical-strip">
      </div>
      <div class="blue-strip vertical-strip">
      </div>
    </div>
  {/if}
  {#if y >= 80}
    <p>maar</p>
    <div class="vertical-strip-box">
      <div class="blue-strip vertical-strip">
      </div>
      <div class="white-strip vertical-strip">
      </div>
      <div class="blue-strip vertical-strip">
      </div>
    </div>
  {/if}
  {#if y >= 90}
    <p>een</p>
    <div class="vertical-strip-box">
      <div class="blue-strip vertical-strip">
      </div>
      <div class="white-strip vertical-strip">
      </div>
      <div class="blue-strip vertical-strip">
      </div>
    </div>
  {/if}
  {#if y >= 100}
    <p>meisje</p>
    <div class="vertical-strip-box" id="first-pink-apparence">
      <div class="blue-strip vertical-strip">
      </div>
      <div class="pink-strip vertical-strip">
      </div>
      <div class="white-strip vertical-strip">
      </div>
      <div class="pink-strip vertical-strip">
      </div>
      <div class="blue-strip vertical-strip">
      </div>
    </div>
  {/if}
  <!--  <div class="horizontal-strip-box">
      <div class="blue-strip horizontal-strip"></div>
      <div class="pink-strip horizontal-strip"></div>
      <div class="white-strip horizontal-strip"></div>
      <div class="pink-strip horizontal-strip"></div>
      <div class="blue-strip horizontal-strip"></div>
    </div-->
</div>
<div>
  {#if y <= 100}
    <div style="
  width: 100%;
  height: 1500px;
"></div>
  {:else}
    <div style="
  width: 100%;
  height: 150px;
"></div>
  {/if}
</div>