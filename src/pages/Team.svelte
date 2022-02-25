<script>
  export let team = "";
  import Button from "../components/Button.svelte";

  let teams = {
    LLL: {
      fullName: "LOUD",
      logo: "../assets/loud.png",
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
      },
      mediaUrls: {
        instagram: "",
        twitter: "",
        youtube: "",
      },
      lastGame: "",
      backgroundPattern: "",
      colors: {
        hero: "bg-slate-900",
        button: "bg-green-600",
      },
    },
  };
</script>

<h1 class="text-6xl">{team}</h1>
<Button
  style="filled"
  href="."
  css={`${teams[team].colors.button} hover:bg-green-400`}>Clique aqui</Button
>

<img src={teams[team].logo} alt={teams[team].logo} />
