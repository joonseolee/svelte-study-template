<script>
  let scoops = 1;
</script>

<label>
  <input type="radio" bind:group={scoops} value={1} />
  One
</label>

<label>
  <input type="radio" bind:group={scoops} value={2} />
  Two
</label>

<label>
  <input type="radio" bind:group={scoops} value={3} />
  Three
</label>

{#if scoops === 1}
  <p>One is selected</p>
{:else if scoops === 2}
  <p>Two is selected</p>
{:else}
  <p>Three is selected</p>
{/if}
