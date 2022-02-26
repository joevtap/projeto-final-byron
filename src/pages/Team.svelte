<script>
  export let team = "";
  import HeroTeam from "../layout-components/HeroTeam.svelte";
  import LastGame from "../layout-components/LastGame.svelte";
  import Players from "../layout-components/Players.svelte";
  import teams from "../teams.json";
</script>

<HeroTeam team={teams[team]} />
<LastGame team={teams[team]} />
<Players team={teams[team]} />
