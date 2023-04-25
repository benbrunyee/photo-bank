<script>
  import Image from "../components/Image.svelte";

  let outerWidth = 0;
</script>

<svelte:window bind:outerWidth />
<div class="flex max-h-full min-h-0 flex-wrap gap-2 overflow-y-auto">
  {#each Array(20) as _}
    <Image width={outerWidth / 5 - 12.75} height={(outerWidth / 5 / 3) * 4} class="bg-cover" />
  {/each}
</div>
