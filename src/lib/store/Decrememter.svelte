<script>
  import { count } from "./status-store";

  function decrease() {
    count.update((n) => n - 1);
  }
</script>

<button on:click={decrease}> - </button>
