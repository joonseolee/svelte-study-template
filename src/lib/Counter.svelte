<script lang="ts">
  let count: number = 0;
  let value = "Hello ";

  $: if (count >= 10) {
    alert("count is dangerously high!");
    count = 9;
  }

  const increment = (event) => {
    console.log("event called");
    console.log(event);
    count += 1;
  };
</script>

<button on:click={increment}>
  Clicks: {count}
  {count < 2 ? "time" : "times"}
</button>

<!-- {value} === value="{value}" -->
Value: <input type="text" {value} />

<style>
  button {
    font-family: inherit;
    font-size: inherit;
    padding: 1em 2em;
    color: #ff3e00;
    background-color: rgba(255, 62, 0, 0.1);
    border-radius: 2em;
    border: 2px solid rgba(255, 62, 0, 0);
    outline: none;
    width: 200px;
    font-variant-numeric: tabular-nums;
    cursor: pointer;
  }

  button:focus {
    border: 2px solid #ff3e00;
  }

  button:active {
    background-color: rgba(255, 62, 0, 0.2);
  }
</style>
