<script lang="ts">
  let m = { x: 0, y: 0 };

  function handleMouseMove(event: MouseEvent) {
    m.x = event.clientX;
    m.y = event.clientY;
  }
</script>

`

<div on:mousemove={handleMouseMove}>
  The mouse position is {m.x} and {m.y}
</div>

<style>
  div {
    width: 100%;
    height: 100%;
  }
</style>
