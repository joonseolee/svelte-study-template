<script lang="ts">
  let cats: any[] = [
    { id: "1", name: "hey1" },
    { id: "2", name: "hey2" },
    { id: "3", name: "hey3" },
  ];
  const name = "sample";
</script>

<ul>
  {#each cats as { id, name }, i}
    <li>
      <a href="www.naver.com">
        {i + 1}: {id}
        {name}
      </a>
    </li>
  {/each}
</ul>
