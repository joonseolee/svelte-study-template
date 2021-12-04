<script>
  import Box from "./Box.svelte";
  import ContactCard from "./ContactCard.svelte";
  import Hoverable from "./Hoverable.svelte";
  import Profile from "./Profile.svelte";
</script>

<Box>
  <h2>Hello!</h2>
  <p>This is a box. It can contain~~</p>
</Box>

<Box />

<ContactCard>
  <span slot="name"> P.Sherrr </span>
  <span slot="address"> Suwon </span>
</ContactCard>

<Hoverable let:hovering>
  <div class:hovering>
    {#if hovering}
      <p>I'm being hovered upon.</p>
    {:else}
      <p>Hover over me!</p>
    {/if}
  </div>
</Hoverable>

<!-- hovering 이라는 변수를 active 에 재할당 -->
<Hoverable let:hovering={active}>
  <!-- class 내에 있는것을 dynamic 하게 바꿔주는듯 Vue -> :class="" 이것과 비슷 -->
  <div class:active>
    {#if active}
      <p>I'm being hovered upon.</p>
    {:else}
      <p>Hover over me!</p>
    {/if}
  </div>
</Hoverable>

<Profile>
  <span slot="name">Bob</span>
  <span slot="email">bob@emaildd.com</span>
</Profile>

<Profile>
  <span slot="name">Bob</span>
  <span slot="phone">01012341234</span>
</Profile>

<style>
  div {
    padding: 1em;
    margin: 0 0 1em 0;
    background-color: #eee;
  }

  .hovering {
    background-color: #ff3e00;
    color: white;
  }
</style>
