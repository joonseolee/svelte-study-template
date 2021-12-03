<script>
  import { createEventDispatcher } from "svelte";

  const dispatch = createEventDispatcher();

  function sayHello() {
    dispatch("message", {
      text: "Hello in here",
    });
    dispatch("message1", {
      text: "message one is here ",
    });
  }
</script>

<button on:click={sayHello}> Click to say Hello </button>
