<script>
  import Decrememter from "./Decrememter.svelte";
  import Incrememter from "./Incrememter.svelte";
  import Resetter from "./Resetter.svelte";
  import { count, elapsed, time, newCount } from "./status-store";

  let count_value;

  const unsubscribe = count.subscribe((value) => {
    count_value = value;
  });

  const formatter = new Intl.DateTimeFormat("en", {
    hour12: true,
    hour: "numeric",
    minute: "2-digit",
    second: "2-digit",
  });
</script>

<h1>The count is {count_value}</h1>
<!-- Auto subscription -->
<h1>The count is {$count}</h1>
<Incrememter />
<Decrememter />
<Resetter />
<h1>The Time is {formatter.format($time)}</h1>
<p>
  The page has been open for
  {$elapsed}
  {$elapsed === 1 ? "second" : "seconds"}
</p>

<div>
  <h1>The Count {$newCount}</h1>
  <button on:click={newCount.increment}>+</button>
  <button on:click={newCount.decrement}>-</button>
  <button on:click={newCount.reset}>reset</button>
</div>
