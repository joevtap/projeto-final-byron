<script>
  import ButtonTeam from "../components/ButtonTeam.svelte";
  import { fly } from "svelte/transition";
  import { onMount } from "svelte";

  onMount(() => {
    window.scrollTo(0, 0);
  });

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
  <img class="h-[230px]" src={team.logo} alt={team.fullName} />

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
      <ButtonTeam
        css={team.colors.button_one}
        cssId="button-heroTeam"
        href="#LastGame"
        style="filled">Último Jogo</ButtonTeam
      >
      <ButtonTeam
        css={team.colors.button_two}
        cssId="button-heroTeamtwo"
        href="#Players"
        style="outline">Equipe CBLOL 2022</ButtonTeam
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

  section h1 {
    overflow: hidden;
    width: 0;
    transform-origin: left;
    animation: wave 1s forwards 200ms steps(20);
  }

  @keyframes wave {
    to {
      width: 360px;
      opacity: 1;
    }
  }
</style>
