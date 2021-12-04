<script lang="ts" context="module">
  export function sayAge() {
    alert("10");
  }
</script>

<script lang="ts">
  function sayName() {
    alert("hello joon");
  }
</script>

<button on:click={sayName}>Click</button>
