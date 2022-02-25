<script>
  import Home from "./pages/Home.svelte";
  import Team from "./pages/Team.svelte";
  import { Router, Route, Link } from "svelte-routing";

  export let url = "";
</script>

<Router {url}>
  <div>
    <Route path="team/:team" let:params><Team team={params.team} /></Route>
    <Route path="/"><Home /></Route>
  </div>
</Router>

<style lang="postcss" global>
  @tailwind base;
  @tailwind components;
  @tailwind utilities;

  body {
    @apply bg-slate-100;
  }
</style>
