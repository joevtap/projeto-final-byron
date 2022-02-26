<script>
  import { onMount } from "svelte";
  import { fade } from "svelte/transition";
  let isLoading = true;

  onMount(() => {
    window.addEventListener("load", () => {
      isLoading = !isLoading;
    });
  });
</script>

{#if isLoading}
  <div
    class="z-50 fixed top-0 left-0 w-screen h-screen bg-slate-50 flex items-center justify-center"
    transition:fade
    class:pointer-events-none={!isLoading}
  >
    <div
      id="spinner"
      class="h-14 w-14 rounded-full border-t-2 border-r-2 border-sky-600"
    />
  </div>
{/if}

<style>
  #spinner {
    animation: spin 600ms linear infinite;
  }

  @keyframes spin {
    to {
      transform: rotate(360deg);
    }
  }
</style>
