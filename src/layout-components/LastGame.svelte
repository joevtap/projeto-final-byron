<script>

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

<section id="LastGame" class="py-20 flex flex-col justify-center items-center px-4 {team.colors.grad_one}">
    <h1
      class="mb-6 font-bold font-['Work_Sans'] text-4xl text-center max-w-6xl {team.colors.title_lastGame}"
    >
      Último Jogo
    </h1>

      <iframe width="1000" height="550" src="{team.lastGame}" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    

    
    {#if team.colors.conteudo_lastGame == "preto"}
      <div class="flex items-center py-10 space-x-20">
        <a href="{team.mediaUrls.instagram}"><img src="../assets/Instagram.png" alt=""></a>
        <a href="{team.mediaUrls.twitter}"><img src="../assets/Twitter.png" alt=""></a>
        <a href="{team.mediaUrls.youtube}"><img src="../assets/Youtube.png" alt=""></a>
      </div>
    {:else if team.colors.conteudo_lastGame == "branco"}
      <div class="flex items-center py-10 space-x-20">
        <a href="{team.mediaUrls.instagram}"><img src="../assets/Instagramb.png" alt=""></a>
        <a href="{team.mediaUrls.twitter}"><img src="../assets/Twitterb.png" alt=""></a>
        <a href="{team.mediaUrls.youtube}"><img src="../assets/Youtubeb.png" alt=""></a>
      </div>
    {/if}
    

</section>

<style>

  @keyframes wave {
    to {
      width: 360px;
      opacity: 1;
    }
  }
</style>
