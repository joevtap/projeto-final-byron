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
    class="bg-sky-500 hover:bg-sky-400 transition-colors rounded-full px-8 flex items-center justify-center h-12 text-white text-base font-bold text-center {css}"
  >
    <slot />
  </a>
{:else}
  <a
    {href}
    id={cssId}
    class=" hover:bg-sky-100 border-2 border-sky-600 transition-colors rounded-full px-8 flex items-center justify-center h-12 text-sky-600 text-base text-center font-bold {css}"
  >
    <slot />
  </a>
{/if}
