<script>
  import { fly } from "svelte/transition";

  let teams = [
    {
      id: 1,
      name: "FURIA Esports",
      shortName: "FUR",
      position: 1,
      win: 7,
      los: 1,
      logo: "assets/furia.png",
    },
    {
      id: 2,
      name: "KaBuM! e-Sports",
      shortName: "KBM",
      position: 2,
      win: 6,
      los: 2,
      logo: "assets/kbm.png",
    },
    {
      id: 3,
      name: "Liberty",
      shortName: "LBR",
      position: 3,
      win: 5,
      los: 3,
      logo: "assets/liberty.png",
    },
    {
      id: 4,
      name: "LOUD",
      shortName: "LBR",
      position: 3,
      win: 5,
      los: 3,
      logo: "assets/loud.png",
    },
    {
      id: 5,
      name: "RED Canids",
      shortName: "RED",
      position: 3,
      win: 5,
      los: 3,
      logo: "assets/red.png",
    },
    {
      id: 6,
      name: "Netshoes Miners",
      shortName: "NMG",
      position: 4,
      win: 4,
      los: 4,
      logo: "assets/netshoesminers.png",
    },
    {
      id: 7,
      name: "paiN Gaming",
      shortName: "PNG",
      position: 4,
      win: 4,
      los: 4,
      logo: "assets/pain.png",
    },
    {
      id: 8,
      name: "Flamengo Esports",
      shortName: "FLA",
      position: 5,
      win: 2,
      los: 6,
      logo: "assets/flamengo.png",
    },
    {
      id: 9,
      name: "INTZ",
      shortName: "ITZ",
      position: 5,
      win: 2,
      los: 6,
      logo: "assets/INTZlogo_square.png",
    },
    {
      id: 10,
      name: "Rengsa Esports",
      shortName: "RNS",
      position: 5,
      win: 2,
      los: 6,
      logo: "assets/rengsa.png",
    },
  ];
  let messages = [
    {
      id: 1,
      image: `https://avatars.dicebear.com/api/identicon/user1451.svg`,
      user: "User #1451",
      message: "#GoFURIA",
    },
    {
      id: 2,
      image: `https://avatars.dicebear.com/api/identicon/user1212.svg`,
      user: "User #1212",
      message: "#GoPAIN",
    },
  ];
  let textInput = "";

  function handleInput() {
    if (textInput) {
      const message = textInput;
      textInput = "";

      const id = messages[messages.length - 1].id + 1;
      const image =
        "https://avatars.dicebear.com/api/identicon/voceehlegal.svg";
      const user = "Você";

      messages = [...messages, { id, message, image, user }];
    }
  }

  function handleEnter(event) {
    if (event.keyCode == 13) {
      handleInput();
    }
  }
</script>

<section class="p-6 pb-[200px]" id="mostre-sua-torcida">
  <div
    class="container flex lg:flex-row items-center p-2 lg:items-stretch flex-col rounded-lg bg-slate-50"
  >
    <div
      id="stats"
      class="flex-grow flex-shrink-0 w-full md:min-w-[560px] lg:max-w-[560px] overflow-y-scroll max-h-[560px] "
    >
      {#each teams as team (team.id)}
        <div class="flex items-center justify-between py-6 pl-4 pr-10">
          <div class="flex items-center justify-between gap-8">
            <span class="text-slate-500 font-medium text-sm"
              >{team.position}º</span
            >
            <img class="w-12 object-contain" src={team.logo} alt={team.name} />
            <div>
              <p class="text-base font-bold text-slate-900">
                {team.name}
              </p>

              <span class="text-slate-600 text-sm font-normal">
                {team.shortName}
              </span>
            </div>
          </div>
          <div>
            <span class="text-green-600 font-medium text-sm">{team.win}V</span>
            <span class="text-red-500 font-medium text-sm">{team.los}D</span>
          </div>
        </div>
      {/each}
    </div>

    <div
      id="chat"
      class="flex flex-col w-full justify-between py-6 md:p-6 gap-6 h-[30rem] lg:h-auto"
    >
      <div
        class="flex flex-col w-full gap-6 overflow-y-scroll overflow-x-hidden"
      >
        {#each messages as message (message.id)}
          <div
            class="flex items-start gap-4"
            transition:fly={{ y: 5, duration: 300 }}
          >
            <img
              class="rounded-full w-12 h-12 object-cover"
              src={message.image}
              alt={message.user}
            />

            <div class="flex flex-col items-start justify-center">
              <p class="text-slate-900 text-base font-bold">{message.user}</p>
              <p class="text-slate-700 text-sm font-normal">
                {message.message}
              </p>
            </div>
          </div>
        {/each}
      </div>
      <div class="flex gap-4">
        <input
          type="text"
          bind:value={textInput}
          on:keyup={handleEnter}
          placeholder="Mande sua mensagem"
          class="h-12 flex-grow rounded-full bg-slate-200 border-slate-300 border-[1px] pl-4 py-2 pr-2 text-slate-800"
        />
        <button
          on:click={handleInput}
          class="rounded-[100%] w-12 h-12 cursor-pointer hover:bg-sky-400 bg-sky-500 transition flex items-center justify-center"
        >
          <img src="assets/arrow.svg" alt="enviar" />
        </button>
      </div>
    </div>
  </div>
</section>

<style>
  section {
    background: linear-gradient(180deg, #f1f5f9 0%, #ffffff 100%);
    opacity: 0;
    transform: translateY(50%);
    animation: fade 600ms forwards 400ms;
  }

  section > div {
    box-shadow: 0px 12px 40px -12px rgba(51, 65, 85, 0.08);
  }

  #stats::-webkit-scrollbar,
  #chat > div:first-child::-webkit-scrollbar {
    width: 6px;
  }

  #stats::-webkit-scrollbar-track,
  #chat > div:first-child:-webkit-scrollbar-track {
    @apply bg-slate-100 rounded-full my-6;
  }

  #stats::-webkit-scrollbar-thumb,
  #chat > div:first-child::-webkit-scrollbar-thumb {
    @apply bg-slate-300 rounded-full;
  }

  @keyframes fade {
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>
