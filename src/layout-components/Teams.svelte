<script>
  import TeamCard from "../components/TeamCard.svelte";

  let teams = {
    "FURIA Esports": {
      name: "FURIA Esports",
      shortName: "FUR",
      image: "assets/furia.png",
      description: "https://www.youtube.com/embed/RK7xvuR45E8",
    },
    "KaBuM! e-Sports": {
      name: "KaBuM! e-Sports",
      shortName: "KBM",
      image: "assets/kbm.png",
      description: "https://www.youtube.com/embed/h8qKUzMLEJc",
    },
    Liberty: {
      name: "Liberty",
      shortName: "LBR",
      image: "assets/liberty.png",
      description: "https://www.youtube.com/embed/U3Qm2RqPVgI",
    },
    LOUD: {
      name: "LOUD",
      shortName: "LLL",
      image: "assets/loud.png",
      description: "https://www.youtube.com/embed/h8qKUzMLEJc",
    },
    "RED Canids": {
      name: "RED Canids",
      shortName: "RED",
      image: "assets/red.png",
      description: "https://www.youtube.com/embed/YRfHC5IL2Fs",
    },
    "Netshoes Miners": {
      name: "Netshoes Miners",
      shortName: "NMG",
      image: "assets/netshoesminers.png",
      description: "https://www.youtube.com/embed/HS1g3PC_-AA",
    },
    "paiN Gaming": {
      name: "paiN Gaming",
      shortName: "PNG",
      image: "assets/pain.png",
      description: "https://www.youtube.com/embed/HS1g3PC_-AA",
    },
    "Flamengo Esports": {
      name: "Flamengo Esports",
      shortName: "FLA",
      image: "assets/flamengo.png",
      description: "https://www.youtube.com/embed/U3Qm2RqPVgI",
    },
    INTZ: {
      name: "INTZ",
      shortName: "ITZ",
      image: "assets/INTZlogo_square.png",
      description: "https://www.youtube.com/embed/YRfHC5IL2Fs",
    },
    "Rengsa Esports": {
      name: "Rengsa Esports",
      shortName: "RNS",
      image: "assets/rengsa.png",
      description: "https://www.youtube.com/embed/RK7xvuR45E8",
    },
  };
</script>

<section class="pt-[94px] pb-[256px]" id="times">
  <h2
    class="mb-6 font-semibold font-['Work_Sans'] text-5xl text-center text-slate-800"
  >
    Conheça os times participantes
  </h2>
  <p
    class="text-slate-600 text-center text-lg mb-20 font-['Work_Sans'] font-medium"
  >
    10 times disputando pelo título de melhor do Brasil
  </p>

  <div class="container flex flex-col gap-6 items-center max-w-[1312px]">
    <div class="flex flex-col md:flex-row gap-6 w-full">
      <TeamCard team={teams["FURIA Esports"]} />
      <TeamCard team={teams["KaBuM! e-Sports"]} />
      <TeamCard team={teams["RED Canids"]} />
    </div>
    <div class="flex flex-col md:flex-row gap-6 w-full">
      <TeamCard team={teams["Liberty"]} />
      <TeamCard team={teams["Netshoes Miners"]} />
      <TeamCard team={teams["LOUD"]} />
      <TeamCard team={teams["paiN Gaming"]} />
    </div>
    <div class="flex flex-col md:flex-row gap-6 w-full">
      <TeamCard team={teams["Rengsa Esports"]} />
      <TeamCard team={teams["Flamengo Esports"]} />
      <TeamCard team={teams["INTZ"]} />
    </div>
  </div>
</section>

<style>
  section {
    background-image: url("/assets/background-pattern.png"),
      linear-gradient(180deg, #f1f5f9 0%, #ffffff 100%);
    box-shadow: 0px 1px 0px rgba(0, 0, 0, 0.12);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }
</style>
