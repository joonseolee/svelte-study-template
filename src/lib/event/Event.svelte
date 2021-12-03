<script>
  import Outer from "./Outer.svelte";

  function handleMessage(event) {
    console.dir(event);
    console.log(event.detail.text);
  }
</script>

<Outer on:message={handleMessage} on:message1={handleMessage} />
