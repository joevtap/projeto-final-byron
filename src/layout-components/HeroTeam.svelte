<script>
  import Button from "../components/Button.svelte";
  import { fly } from "svelte/transition";

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

  let visible = false;

  setTimeout(() => {
    visible = true;
  }, 500);
</script>

<section
  class="py-20 flex flex-col justify-center items-center px-4 h-[678px] {team
    .colors.hero}"
>
  <img class="h-[230px] mb-8" src={team.logo} alt={team.fullName} />

  {#if visible}
    <h1
      transition:fly={{ y: 10, duration: 600 }}
      class="mb-6 font-bold font-['Work_Sans'] text-6xl text-center max-w-4xl {team
        .colors.title_main}"
    >
      {team.fullName}
    </h1>

    <p
      transition:fly={{ y: 10, duration: 600, delay: 100 }}
      class="text-slate-600 text-center text-lg mb-16 font-['Work_Sans'] font-medium"
    >
      {team.hashtag}
    </p>
    <div
      transition:fly={{ y: 10, duration: 600, delay: 200 }}
      class="flex flex-col items-center md:flex-row"
    >
      <Button
        css={team.colors.button_one + " mb-6 mr-0 md:mb-0 md:mr-6"}
        cssId="button-heroTeam"
        href="#LastGame"
        style="filled">Último Jogo</Button
      >
      <Button
        css={team.colors.button_two}
        cssId="button-heroTeamtwo"
        href="#Players"
        style="outline">Equipe CBLOL 2022</Button
      >
    </div>
  {/if}
</section>

<style>
  section {
    background-image: url("/assets/background-pattern.png");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }
</style>
