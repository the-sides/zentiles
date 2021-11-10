<script>
  import { onDestroy } from "svelte";
  import Tile from "./Tile.svelte";
  // Array of columns
  let columns = [];

  // Build board with columns, and a cells making up rows inside
  for (let columnIndex = 0; columnIndex < 10; columnIndex++) {
    columns = [...columns, []];
    for (let rowIndex = 0; rowIndex < 10; rowIndex++) {
      const cellValue = Math.round(Math.random() * 10);
      if (!columns[columnIndex][rowIndex]) columns[columnIndex][rowIndex] = [];
      columns[columnIndex][rowIndex].push(cellValue);
    }
  }
</script>

<div class="flex justify-center pb-12">
  {#each columns as boardCol}
    <div class="mx-2 ">
      <!-- Cells moving down -->
      {#each boardCol as cell}
        <div class="slot mx-2 w-8 h-3 overflow-visible relative">
          <Tile label={cell} />
        </div>
      {/each}
    </div>
  {/each}
</div>

<div class="mt-8 mx-auto flex justify-center w-[160px] h-10 bg-blue-200">
  <div class="slot relative w-1/3"><Tile label="4" /></div>
  <div class="slot relative  w-1/3"><Tile label="4" /></div>
  <div class="slot relative  w-1/3"><Tile label="4" /></div>
</div>
