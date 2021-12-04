<script>
  import { count } from "./status-store";

  function increment() {
    count.update((n) => n + 1);
  }
</script>

<button on:click={increment}> + </button>
