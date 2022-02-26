<script>
  import PlayerCard from "../components/PlayerCard.svelte";

  export let team = {
    firstName: "",
    fullName: "",
    hashtag: "",
    logo: "",
    players: {
      top: {
        name: "",
        pic: "",
        role: "",
        roleImage: "",
      },
      jg: {
        name: "",
        pic: "",
        role: "",
        roleImage: "",
      },
      mid: {
        name: "",
        pic: "",
        role: "",
        roleImage: "",
      },
      bot: {
        name: "",
        pic: "",
        role: "",
        roleImage: "",
      },
      sup: {
        name: "",
        pic: "",
        role: "",
        roleImage: "",
      },
    },
    mediaUrls: {
      instagram: "",
      twitter: "",
      youtube: "",
    },
    lastGame: "",
    backgroundPattern: "",
    colors: {
      hero: "",
      title_main: "",
      hash: "",
      button_one: "",
      button_two: "",
      grad_one: "",
      grad_two: "",
      title_lastGame: "",
      conteudo_lastGame: "",
      title_players: "",
    },
  };
</script>

<section
  id="Players"
  class="py-20 flex flex-col justify-center items-center px-4 bg-[url('{team.backgroundPattern}')] {team
    .colors.grad_two}"
>
  <h2
    class="{team.colors.title_players} p-3 border-gray-200 text-3xl font-bold"
  >
    Equipe titular {team.firstName} CBLOL 2022
  </h2>

  <div class="container flex flex-col gap-4 py-10 items-center">
    <div
      class="flex flex-col justify-center items-center lg:flex-row gap-6 w-full"
    >
      <PlayerCard player={team.players.top} />
      <PlayerCard player={team.players.jg} />
      <PlayerCard player={team.players.mid} />
    </div>
    <div
      class="flex flex-col justify-center items-center lg:flex-row gap-6 w-full"
    >
      <PlayerCard player={team.players.bot} />
      <PlayerCard player={team.players.sup} />
    </div>
  </div>
</section>

<style>
  section {
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }

  @keyframes wave {
    to {
      width: 360px;
      opacity: 1;
    }
  }
</style>
