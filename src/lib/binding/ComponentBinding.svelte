<script>
  import Keypad from "./Keypad.svelte";
  import keypad from "./Keypad.svelte";
  let pin;

  $: view = pin ? pin.replace(/\d(?!$)/g, "•") : "enter your pin!!!";

  function handleSubmit() {
    alert(`submit ${pin}`);
  }
</script>

<h1 style="color: {pin ? '#333' : '#ccc'}">{view}</h1>

<Keypad bind:value={pin} on:submit={handleSubmit} />
