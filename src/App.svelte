<script>
  import Navbar from "./components/Navbar.svelte";
  import Hero from "./layout-components/Hero.svelte";
</script>

<div>
  <Navbar />
  <Hero />
</div>

<style lang="postcss" global>
  @tailwind base;
  @tailwind components;
  @tailwind utilities;

  :global(body) {
    @apply bg-slate-100;
  }
</style>
