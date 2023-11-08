<script>
  import data from "../data.json";
  import { push } from "svelte-spa-router";
</script>

<div class="p-4">
  <ul class="menu bg-base-200 w-full rounded-box">
    {#each data as x}
      <li><a href="#/doa/{x.id}">{x.judul}</a></li>
    {/each}
  </ul>
</div>
