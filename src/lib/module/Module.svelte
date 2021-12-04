<script lang="ts">
  import Component, { sayAge } from "./Component.svelte";
</script>

<Component />
<button on:click={sayAge}>Click</button>
