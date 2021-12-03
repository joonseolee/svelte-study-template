<script lang="ts">
  function handleClick() {
    alert("only once called");
  }
</script>

<button on:click|once={handleClick}> Click me </button>
