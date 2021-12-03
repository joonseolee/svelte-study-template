<script lang="ts">
  let name = "";
</script>

<input type="text" bind:value={name} placeholder="enter your name" />
<p>Hello {name || "stranger"}</p>
