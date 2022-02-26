<script>
  export let style = "filled"; // filled or outline
  export let css = "";
  export let cssId = "";
  export let href = "";
</script>

{#if style == "filled"}
  <a
    {href}
    id={cssId}
    class="transition-colors rounded-full px-8 flex items-center justify-center h-12 text-base font-bold text-center {css} sm:m-2"
  >
    <slot />
  </a>
{:else}
  <a
    {href}
    id={cssId}
    class="border-2 transition-colors rounded-full px-8 flex items-center justify-center h-12 text-base text-center font-bold {css}"
  >
    <slot />
  </a>
{/if}
