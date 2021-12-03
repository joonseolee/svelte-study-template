<script>
  let yes = false;
</script>

<label>
  <input type="checkbox" bind:checked={yes} />
  Yes! Send me regular email spam
</label>

{#if yes}
  <p>Thannk you we will</p>
{:else}
  <p>You must opt</p>
{/if}

<button disabled={!yes}> Subscribe </button>
