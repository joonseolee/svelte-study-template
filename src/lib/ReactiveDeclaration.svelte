<script lang="ts">
  let count = 1;

  /** listen */
  $: doubled = count * 2;
  $: quadrupled = doubled * 2;

  const handleClick = () => {
    count += 1;
  };
</script>

<button on:click={handleClick}>
  Count: {count}
</button>

<p>{count} * 2 = {doubled}</p>
<p>{doubled} * 2 = {quadrupled}</p>
