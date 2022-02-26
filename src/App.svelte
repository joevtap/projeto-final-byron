<script>
  import Home from "./pages/Home.svelte";
  import Team from "./pages/Team.svelte";
  import Footer from "./layout-components/Footer.svelte";
  import { Router, Route } from "svelte-routing";

  export let url = "";
</script>

<Router {url}>
  <div>
    <Route path="team/:team" let:params><Team team={params.team} /></Route>
    <Route path="/"><Home /></Route>
  </div>
  <Footer />
</Router>

<style lang="postcss" global>
  @tailwind base;
  @tailwind components;
  @tailwind utilities;

  body {
    @apply bg-slate-100;
  }
</style>
