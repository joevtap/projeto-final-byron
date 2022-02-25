<script>
  import Button from "../components/Button.svelte";
  import { fly } from "svelte/transition";

  let visible = false;

  setTimeout(() => {
    visible = true;
  }, 500);
</script>

<section class="py-48 flex flex-col justify-center items-center px-4 h-[678px]">
  {#if visible}
    <h1
      transition:fly={{ y: 10, duration: 600 }}
      class="mb-6 font-bold font-['Work_Sans'] text-6xl text-center max-w-4xl text-slate-800"
    >
      Mostre sua torcida para o seu time no <span
        class="text-sky-500 font-['Work_Sans']">CBLOL 2022</span
      >
    </h1>
    <p
      transition:fly={{ y: 10, duration: 600, delay: 100 }}
      class="text-slate-600 text-center text-lg mb-16 font-['Work_Sans'] font-medium"
    >
      Chat e estatísticas em tempo real para torcer e acompanhar
    </p>
    <div
      transition:fly={{ y: 10, duration: 600, delay: 200 }}
      class="flex flex-col items-center md:flex-row"
    >
      <Button cssId="button-hero" href="#times" style="filled"
        >Conheça os times</Button
      >
      <Button href="#mostre-sua-torcida" style="outline"
        >Mostre sua torcida</Button
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

  section h1 span {
    overflow: hidden;
    white-space: nowrap;
    display: inline-flex;
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
