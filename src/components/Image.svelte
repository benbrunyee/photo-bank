<script lang="ts">
  import Skeleton from "./Skeleton.svelte";
  export let containerClasses = "";
  export let loadingContainerClasses = "";
  export let onLoad = () => {};
  export let width: number | undefined = undefined;
  export let height: number | undefined = undefined;

  let imageLoading = true;

  function handleLoad() {
    imageLoading = false;
    onLoad();
  }
</script>

<div
  class="relative {containerClasses}"
  style="{typeof width !== 'undefined' ? `width: ${width}px;` : ''} {typeof height !== 'undefined'
    ? `height: ${height}px`
    : ''}"
>
  <img
    {...$$restProps}
    alt={$$props.alt}
    on:load={handleLoad}
    {...width ? { width } : {}}
    {...height ? { height } : {}}
  />
  {#if imageLoading}
    <Skeleton
      class={loadingContainerClasses}
      style="{typeof width !== 'undefined' ? `width: ${width}px;` : ''} {typeof height !==
      'undefined'
        ? `height: ${height}px`
        : ''}"
    />
  {/if}
</div>
