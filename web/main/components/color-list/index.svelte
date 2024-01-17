<script lang="ts">
  export let value: string = "#ffffff";

  // export let change: (value: string) => void;

  const colors = ["#ffffff", "#eeeeee", "#dddddd", "#888888", "#000000"];

  const handleSelect = (color: string) => {
    console.log(color);
    value = color;
  };
</script>

<div class="flex">
  {#each colors as color}
    <div style="background-color:{color};width:20px;height:20px;margin-left:10px;{value === color ? 'border-color:red; border-width:1px;' : ''}" on:click={() => handleSelect(color)} />
  {/each}
</div>
