<script lang="ts">
  import "../app.css";
  import UploadButton from "../components/UploadButton.svelte";
</script>

<div
  class="flex h-full min-h-0 w-full flex-col gap-2 bg-gradient-to-tl from-blue-950 to-blue-900 p-2"
>
  <div class="flex-1">
    <slot />
  </div>
  <UploadButton />
</div>

{#if import.meta.env.DEV}
  <style lang="postcss">
    * {
      outline: 1px solid red;
    }
  </style>
{/if}
