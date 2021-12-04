<script>
  import { onMount, onDestroy, beforeUpdate, afterUpdate, tick } from "svelte";

  onMount(() => {
    console.log("onMount");
  });

  onDestroy(() => {
    console.log("onDestory");
  });

  beforeUpdate(() => {
    console.log("beforeUpdate");
  });

  afterUpdate(() => {
    console.log("afterUpdate");
  });

  let isShow = false;
  let input;

  async function handleClick() {
    isShow = !isShow;

    // 화면이 렌더링될때까지 기다린다.
    await tick();

    if (isShow) {
      input && input.focus();
    }
  }
</script>

<div>
  <button on:click={handleClick}>Click</button>
  {#if isShow}
    <input type="text" bind:this={input} />
  {/if}
</div>
