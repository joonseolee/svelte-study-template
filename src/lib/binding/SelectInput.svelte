<script>
  let questions = [
    { id: 1, text: "where are you headed1?" },
    { id: 2, text: "where are you headed2?" },
    { id: 3, text: "where are you headed3?" },
  ];

  let selected;

  let answer = "";

  function handleSubmit() {
    console.log(`id - ${selected.id}, answer - ${answer}`);
  }
</script>

<form on:submit|preventDefault={handleSubmit}>
  <select bind:value={selected} on:change={() => (answer = "")}>
    {#each questions as question}
      <option value={question}>{question.text}</option>
    {/each}
  </select>

  <input bind:value={answer} />

  <button disabled={!answer} type="submit"> Submit </button>
</form>
