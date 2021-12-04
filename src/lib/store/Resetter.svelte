<script>
  import { count } from "./status-store";
  function reset() {
    count.set(0);
  }
</script>

<button on:click={reset}> reset </button>
