<script>
  export let team = "";
  import HeroTeam from "../layout-components/HeroTeam.svelte";
  import LastGame from "../layout-components/LastGame.svelte";
  import Players from "../layout-components/Players.svelte";
  import Navbar from "../components/Navbar.svelte";
  import { onMount } from "svelte";

  onMount(() => {
    window.scrollTo(0, 0);
  });

  let teams = {
    // LOUD
    LLL: {
      firstName: "LOUD",
      fullName: "LOUD",
      hashtag: "#GOLOUD",
      logo: "../assets/loud.png",
      players: {
        top: {
          name: "Robo",
          pic: "../assets/LOUD/robo.png",
          role: "Topo",
          roleImage: "../assets/LOUD/top_loud.png",
        },
        jg: {
          name: "Tay",
          pic: "../assets/LOUD/tay.png",
          role: "Caçador",
          roleImage: "../assets/jg.png",
        },
        mid: {
          name: "Tinowns",
          pic: "../assets/LOUD/tinowns.png",
          role: "Meio",
          roleImage: "../assets/LOUD/mid_loud.png",
        },
        bot: {
          name: "DudsTheBoy",
          pic: "../assets/LOUD/dudstheboy.png",
          role: "Atirador",
          roleImage: "../assets/LOUD/bot_loud.png",
        },
        sup: {
          name: "Ceos",
          pic: "../assets/LOUD/ceos.png",
          role: "Suporte",
          roleImage: "../assets/sup.png",
        },
      },
      mediaUrls: {
        instagram: "https://www.instagram.com/loudgg/",
        twitter: "https://twitter.com/LOUDgg",
        youtube: "https://www.youtube.com/loudgg",
      },
      lastGame: "https://www.youtube.com/embed/76EPyA_Ci64",
      backgroundPattern: "../assets/LOUD/p_loud.svg",
      colors: {
        hero: "bg-black",
        title_main: "text-white",
        hash: "text-gray-100",
        button_one: "bg-lime-400 hover:bg-lime-300 !text-black",
        button_two:
          "!text-lime-400 border-lime-400 hover:bg-lime-400 hover:!text-black border-lime-400",
        grad_one: "bg-gradient-to-b from-black to-white",
        grad_two: "bg-gradient-to-b from-white to-black",
        title_lastGame: "text-lime-400",
        conteudo_lastGame: "preto",
        title_players: "bg-black text-lime-400 rounded-md",
      },
    },

    // FURIA
    FUR: {
      firstName: "FURIA",
      fullName: "FURIA Esports",
      hashtag: "#GOFURIA",
      logo: "../assets/furia.png",
      players: {
        top: {
          name: "fNb",
          pic: "../assets/FURIA/fnb.png",
          role: "Topo",
          roleImage: "../assets/FURIA/top_fur.png",
        },
        jg: {
          name: "Ranger",
          pic: "../assets/FURIA/ranger.png",
          role: "Caçador",
          roleImage: "../assets/jg.png",
        },
        mid: {
          name: "Envy",
          pic: "../assets/FURIA/envy.png",
          role: "Meio",
          roleImage: "../assets/FURIA/mid_fur.png",
        },
        bot: {
          name: "Netuno",
          pic: "../assets/FURIA/netuno.png",
          role: "Atirador",
          roleImage: "../assets/FURIA/bot_fur.png",
        },
        sup: {
          name: "RedBert",
          pic: "../assets/FURIA/redbert.png",
          role: "Suporte",
          roleImage: "../assets/sup.png",
        },
      },
      mediaUrls: {
        instagram: "https://www.instagram.com/furiagg/",
        twitter: "https://twitter.com/furia",
        youtube: "https://www.youtube.com/FURIAgg",
      },
      lastGame: "https://www.youtube.com/embed/76EPyA_Ci64",
      backgroundPattern: "../assets/FURIA/p_furia.svg",
      colors: {
        hero: "bg-black",
        title_main: "text-white",
        hash: "text-slate-100",
        button_one:
          "bg-white !text-zinc-900 hover:!bg-transparent border-white hover:border-2 hover:!text-white",
        button_two:
          "text-white border-white hover:bg-white hover:!text-zinc-900",
        grad_one: "bg-gradient-to-b from-black to-white",
        grad_two: "bg-gradient-to-b from-white to-black",
        title_lastGame: "text-white",
        conteudo_lastGame: "preto",
        title_players: "bg-white text-black rounded-md",
      },
    },

    // KABUM
    KBM: {
      firstName: "KaBuM!",
      fullName: "KaBuM! e-Sports",
      hashtag: "#GOKBM",
      logo: "../assets/kbm.png",
      players: {
        top: {
          name: "Parang",
          pic: "../assets/KABUM/parang.png",
          role: "Topo",
          roleImage: "../assets/KABUM/top_kbm.png",
        },
        jg: {
          name: "Wiz",
          pic: "../assets/KABUM/wiz.png",
          role: "Caçador",
          roleImage: "../assets/jg.png",
        },
        mid: {
          name: "Hauz",
          pic: "../assets/KABUM/hauz.png",
          role: "Meio",
          roleImage: "../assets/KABUM/mid_kbm.png",
        },
        bot: {
          name: "Disave",
          pic: "../assets/KABUM/disave.png",
          role: "Atirador",
          roleImage: "../assets/KABUM/bot_kbm.png",
        },
        sup: {
          name: "Scuro",
          pic: "../assets/KABUM/scuro.png",
          role: "Suporte",
          roleImage: "../assets/sup.png",
        },
      },
      mediaUrls: {
        instagram: "https://www.instagram.com/kabumesports/",
        twitter: "https://twitter.com/KaBuMESports",
        youtube: "https://www.youtube.com/kabumesports",
      },
      lastGame: "https://www.youtube.com/embed/MZmSIkUUihU",
      backgroundPattern: "../assets/KABUM/p_kabum.svg",
      colors: {
        hero: "bg-orange-700",
        title_main: "text-white",
        hash: "text-gray-100",
        button_one:
          "bg-black !text-white hover:bg-transparent border-2 border-black hover:!text-black",
        button_two: "!text-black border-black hover:bg-black hover:!text-white",
        grad_one: "bg-gradient-to-b from-orange-700 to-black",
        grad_two: "bg-gradient-to-b from-black to-zinc-300",
        title_lastGame: "text-black",
        conteudo_lastGame: "branco",
        title_players: "bg-white text-orange-700 rounded-md",
      },
    },

    // FLAMENGO
    FLA: {
      firstName: "Flamengo",
      fullName: "Flamengo Esports",
      hashtag: "#GOFLA",
      logo: "../assets/flamengo.png",
      players: {
        top: {
          name: "Boal",
          pic: "../assets/FLAMENGO/boal.png",
          role: "Topo",
          roleImage: "../assets/FLAMENGO/top_fla.png",
        },
        jg: {
          name: "Asta",
          pic: "../assets/FLAMENGO/asta.png",
          role: "Caçador",
          roleImage: "../assets/jg.png",
        },
        mid: {
          name: "Tutsz",
          pic: "../assets/FLAMENGO/tutsz.png",
          role: "Meio",
          roleImage: "../assets/FLAMENGO/mid_fla.png",
        },
        bot: {
          name: "Flare",
          pic: "../assets/FLAMENGO/flare.png",
          role: "Atirador",
          roleImage: "../assets/FLAMENGO/bot_fla.png",
        },
        sup: {
          name: "Kuri",
          pic: "../assets/FLAMENGO/kuri.png",
          role: "Suporte",
          roleImage: "../assets/sup.png",
        },
      },
      mediaUrls: {
        instagram: "https://www.instagram.com/flaesports/",
        twitter: "https://twitter.com/flaesports",
        youtube: "https://www.youtube.com/channel/UCqN_gtT3fqdn4KXdLLSqaHQ",
      },
      lastGame: "https://www.youtube.com/embed/W25sM_D4ExU",
      backgroundPattern: "../assets/FLAMENGO/p_fla.svg",
      colors: {
        hero: "bg-white",
        title_main: "text-black",
        hash: "text-gray-500",
        button_one:
          "bg-red-700 text-white hover:bg-transparent hover:!text-red-700 border-2 border-red-700",
        button_two:
          "!text-red-700 border-red-700 hover:bg-red-700 hover:!text-white",
        grad_one: "bg-gradient-to-b from-white to-red-700",
        grad_two: "bg-gradient-to-b from-red-700 to-black",
        title_lastGame: "text-black",
        conteudo_lastGame: "preto",
        title_players: "bg-white text-red-700 rounded-md",
      },
    },

    // PAIN
    PNG: {
      firstName: "paiN",
      fullName: "paiN Gaming",
      hashtag: "#GOPAIN",
      logo: "../assets/pain.png",
      players: {
        top: {
          name: "Wizer",
          pic: "../assets/PAIN/wizer.png",
          role: "Topo",
          roleImage: "../assets/PAIN/top_pain.png",
        },
        jg: {
          name: "CarioK",
          pic: "../assets/PAIN/cariok.png",
          role: "Caçador",
          roleImage: "../assets/jg.png",
        },
        mid: {
          name: "dyNquedo",
          pic: "../assets/PAIN/dynquedo.png",
          role: "Meio",
          roleImage: "../assets/PAIN/mid_pain.png",
        },
        bot: {
          name: "Trigo",
          pic: "../assets/PAIN/trigo.png",
          role: "Atirador",
          roleImage: "../assets/PAIN/bot_pain.png",
        },
        sup: {
          name: "Damage",
          pic: "../assets/PAIN/damage.png",
          role: "Suporte",
          roleImage: "../assets/sup.png",
        },
      },
      mediaUrls: {
        instagram: "https://www.instagram.com/paingamingbr/",
        twitter: "https://twitter.com/paiNGamingBR",
        youtube: "https://www.youtube.com/c/paingamingbr",
      },
      lastGame: "https://www.youtube.com/embed/thd8FBXbasY",
      backgroundPattern: "../assets/PAIN/p_pain.svg",
      colors: {
        hero: "bg-white",
        title_main: "text-black",
        hash: "text-gray-500",
        button_one:
          "bg-red-500 text-white hover:bg-transparent hover:!text-red-500 border-2 border-red-500",
        button_two:
          "!text-red-500 border-red-500 hover:bg-red-500 hover:!text-white",
        grad_one: "bg-gradient-to-b from-white to-red-500",
        grad_two: "bg-gradient-to-b from-red-500 to-black",
        title_lastGame: "text-black",
        conteudo_lastGame: "preto",
        title_players: "bg-white text-red-500 rounded-md",
      },
    },

    // RED
    RED: {
      firstName: "RED",
      fullName: "RED Canids Kalunga",
      hashtag: "#GORED",
      logo: "../assets/red.png",
      players: {
        top: {
          name: "Guigo",
          pic: "../assets/RED/guigo.png",
          role: "Topo",
          roleImage: "../assets/RED/top_red.png",
        },
        jg: {
          name: "Aegis",
          pic: "../assets/RED/aegis.png",
          role: "Caçador",
          roleImage: "../assets/jg.png",
        },
        mid: {
          name: "Avenger",
          pic: "../assets/RED/avenger.png",
          role: "Meio",
          roleImage: "../assets/RED/mid_red.png",
        },
        bot: {
          name: "TitaN",
          pic: "../assets/RED/titan.png",
          role: "Atirador",
          roleImage: "../assets/RED/bot_red.png",
        },
        sup: {
          name: "Jojo",
          pic: "../assets/RED/jojo.png",
          role: "Suporte",
          roleImage: "../assets/sup.png",
        },
      },
      mediaUrls: {
        instagram: "https://www.instagram.com/redcanids/",
        twitter: "https://twitter.com/REDCanids",
        youtube: "https://www.youtube.com/RedCanidsBR",
      },
      lastGame: "https://www.youtube.com/embed/Tf7ed7mi2rI",
      backgroundPattern: "../assets/RED/p_red.svg",
      colors: {
        hero: "bg-black",
        title_main: "text-white",
        hash: "text-gray-100",
        button_one:
          "bg-red-500 text-white hover:bg-transparent text-red-500 border-2 border-red-500",
        button_two: "text-red-500 border-red-500 hover:bg-red-500 text-white",
        grad_one: "bg-gradient-to-b from-black to-red-800",
        grad_two: "bg-gradient-to-b from-red-800 to-black",
        title_lastGame: "text-white",
        conteudo_lastGame: "branco",
        title_players: "bg-white text-red-800 rounded-md",
      },
    },

    // INTZ
    ITZ: {
      firstName: "INTZ",
      fullName: "INTZ eSports",
      hashtag: "#GOINTZ",
      logo: "../assets/INTZlogo_square.png",
      players: {
        top: {
          name: "Tyrin",
          pic: "../assets/INTZ/tyrin.png",
          role: "Topo",
          roleImage: "../assets/INTZ/top_intz.png",
        },
        jg: {
          name: "Yampi",
          pic: "../assets/INTZ/yampi.png",
          role: "Caçador",
          roleImage: "../assets/jg.png",
        },
        mid: {
          name: "Kick",
          pic: "../assets/INTZ/kick.png",
          role: "Meio",
          roleImage: "../assets/INTZ/mid_intz.png",
        },
        bot: {
          name: "Mica0",
          pic: "../assets/INTZ/mica0.png",
          role: "Atirador",
          roleImage: "../assets/INTZ/bot_intz.png",
        },
        sup: {
          name: "Decoy",
          pic: "../assets/INTZ/decoy.png",
          role: "Suporte",
          roleImage: "../assets/sup.png",
        },
      },
      mediaUrls: {
        instagram: "https://www.instagram.com/intzesports/",
        twitter: "https://twitter.com/intz",
        youtube: "https://www.youtube.com/user/INTZeSports",
      },
      lastGame: "https://www.youtube.com/embed/MZmSIkUUihU",
      backgroundPattern: "../assets/INTZ/p_intz.svg",
      colors: {
        hero: "bg-zinc-100",
        title_main: "text-black",
        hash: "text-gray-700",
        button_one:
          "bg-black text-white hover:bg-transparent hover:!text-black border-2 border-black",
        button_two: "!text-black border-black hover:bg-black hover:!text-white",
        grad_one: "bg-gradient-to-b from-zinc-100 to-black",
        grad_two: "bg-gradient-to-b from-black to-zinc-100",
        title_lastGame: "text-black",
        conteudo_lastGame: "branco",
        title_players: "bg-white text-black rounded-md",
      },
    },

    // MINERS
    NMG: {
      firstName: "Miners",
      fullName: "Netshoes Miners",
      hashtag: "#GOMINERS",
      logo: "../assets/netshoesminers.png",
      players: {
        top: {
          name: "DoRun",
          pic: "../assets/MINERS/dorun.png",
          role: "Topo",
          roleImage: "../assets/MINERS/top_miners.png",
        },
        jg: {
          name: "Croc",
          pic: "../assets/MINERS/croc.png",
          role: "Caçador",
          roleImage: "../assets/jg.png",
        },
        mid: {
          name: "Anyyy",
          pic: "../assets/MINERS/anyyy.png",
          role: "Meio",
          roleImage: "../assets/MINERS/mid_miners.png",
        },
        bot: {
          name: "Celo",
          pic: "../assets/MINERS/celo.png",
          role: "Atirador",
          roleImage: "../assets/MINERS/bot_miners.png",
        },
        sup: {
          name: "Hawk",
          pic: "../assets/MINERS/hawk.png",
          role: "Suporte",
          roleImage: "../assets/sup.png",
        },
      },
      mediaUrls: {
        instagram: "https://www.instagram.com/miners.gg/",
        twitter: "https://twitter.com/minersgg",
        youtube: "https://www.youtube.com/channel/UCNH_VIASvRytiiUzEbS5lgA",
      },
      lastGame: "https://www.youtube.com/embed/W25sM_D4ExU",
      backgroundPattern: "../assets/MINERS/p_miners.svg",
      colors: {
        hero: "bg-indigo-900",
        title_main: "text-white",
        hash: "text-gray-100",
        button_one:
          "bg-red-600 text-white hover:bg-transparent hover:!text-red-600 border-2 border-red-600",
        button_two:
          "!text-red-600 border-red-600 hover:bg-red-600 hover:!text-white",
        grad_one: "bg-gradient-to-b from-indigo-900 to-red-600",
        grad_two: "bg-gradient-to-b from-red-600 to-white",
        title_lastGame: "text-white",
        conteudo_lastGame: "branco",
        title_players: "bg-white text-indigo-900 rounded-md",
      },
    },

    // LIBERTY
    LBR: {
      firstName: "Liberty",
      fullName: "Liberty Esports",
      hashtag: "#GOLIBERTY",
      logo: "../assets/liberty.png",
      players: {
        top: {
          name: "Kiari",
          pic: "../assets/LIBERTY/kiari.png",
          role: "Topo",
          roleImage: "../assets/LIBERTY/top_liberty.png",
        },
        jg: {
          name: "Disamis",
          pic: "../assets/LIBERTY/disamis.png",
          role: "Caçador",
          roleImage: "../assets/jg.png",
        },
        mid: {
          name: "Krastyel",
          pic: "../assets/LIBERTY/krastyel.png",
          role: "Meio",
          roleImage: "../assets/LIBERTY/mid_liberty.png",
        },
        bot: {
          name: "Matsukase",
          pic: "../assets/LIBERTY/matsukase.png",
          role: "Atirador",
          roleImage: "../assets/LIBERTY/bot_liberty.png",
        },
        sup: {
          name: "Wos",
          pic: "../assets/LIBERTY/wos.png",
          role: "Suporte",
          roleImage: "../assets/sup.png",
        },
      },
      mediaUrls: {
        instagram: "https://www.instagram.com/libertyesports/",
        twitter: "https://twitter.com/libertyesports",
        youtube: "https://www.youtube.com/c/libertyesports",
      },
      lastGame: "https://www.youtube.com/embed/thd8FBXbasY",
      backgroundPattern: "../assets/LIBERTY/p_liberty.svg",
      colors: {
        hero: "bg-black",
        title_main: "text-white",
        hash: "text-gray-100",
        button_one:
          "bg-cyan-300 !text-black hover:bg-transparent hover:!text-cyan-300 border-2 border-cyan-300",
        button_two:
          "text-cyan-300 border-cyan-300 hover:bg-cyan-300 hover:!text-black",
        grad_one: "bg-gradient-to-b from-black to-cyan-300",
        grad_two: "bg-gradient-to-b from-cyan-300 to-black",
        title_lastGame: "text-white",
        conteudo_lastGame: "preto",
        title_players: "bg-white text-blue-900 rounded-md",
      },
    },

    // RENSGA
    RNS: {
      firstName: "Rensga",
      fullName: "Rensga Esports",
      hashtag: "#GORENSGA",
      logo: "../assets/rengsa.png",
      players: {
        top: {
          name: "Ayel",
          pic: "../assets/RENSGA/ayel.png",
          role: "Topo",
          roleImage: "../assets/RENSGA/top_rensga.png",
        },
        jg: {
          name: "Minerva",
          pic: "../assets/RENSGA/minerva.png",
          role: "Caçador",
          roleImage: "../assets/jg.png",
        },
        mid: {
          name: "Goku",
          pic: "../assets/RENSGA/goku.png",
          role: "Meio",
          roleImage: "../assets/RENSGA/mid_rensga.png",
        },
        bot: {
          name: "Hades",
          pic: "../assets/RENSGA/hades.png",
          role: "Atirador",
          roleImage: "../assets/RENSGA/bot_rensga.png",
        },
        sup: {
          name: "Guard",
          pic: "../assets/RENSGA/guard.png",
          role: "Suporte",
          roleImage: "../assets/sup.png",
        },
      },
      mediaUrls: {
        instagram: "https://www.instagram.com/rensgaesports/",
        twitter: "https://twitter.com/Rensgaesports",
        youtube: "https://www.youtube.com/channel/UCnEeud3Cq4dqAbKknbzWkkA",
      },
      lastGame: "https://www.youtube.com/embed/Tf7ed7mi2rI",
      backgroundPattern: "../assets/RENSGA/p_rensga.svg",
      colors: {
        hero: "bg-blue-800",
        title_main: "text-yellow-500",
        hash: "text-sky-500",
        button_one:
          "bg-yellow-500 !text-blue-800 hover:bg-transparent border-2 border-yellow-500 hover:!text-yellow-500",
        button_two:
          "text-yellow-500 border-yellow-500 hover:bg-yellow-500 hover:!text-blue-800",
        grad_one: "bg-gradient-to-b from-blue-800 to-sky-500",
        grad_two: "bg-gradient-to-b from-sky-500 to-blue-800",
        title_lastGame: "text-black",
        conteudo_lastGame: "branco",
        title_players: "bg-white text-blue-800 rounded-md",
      },
    },
  };
</script>

<Navbar type="back" color={teams[team].colors.title_main} />
<HeroTeam team={teams[team]} />
<LastGame team={teams[team]} />
<Players team={teams[team]} />
