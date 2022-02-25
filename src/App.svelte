<script>
  import Navbar from "./components/Navbar.svelte";
  import Hero from "./layout-components/Hero.svelte";
  import Chat from "./layout-components/Chat.svelte";
  import Teams from "./layout-components/Teams.svelte";
</script>

<div>
  <Navbar />
  <Hero />
  <Chat />
  <Teams />
</div>

<style lang="postcss" global>
  @tailwind base;
  @tailwind components;
  @tailwind utilities;

  :global(body) {
    @apply bg-slate-100;
  }
</style>
