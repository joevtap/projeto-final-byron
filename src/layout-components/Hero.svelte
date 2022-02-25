<script>
  import Button from "../components/Button.svelte";
</script>

<section class="py-48 flex flex-col justify-center items-center px-4">
  <h1
    class="mb-6 font-bold font-['Work_Sans'] text-6xl text-center max-w-4xl text-slate-800"
  >
    Mostre sua torcida para o seu time no <span
      class="text-sky-500 font-['Work_Sans']">CBLOL 2022</span
    >
  </h1>
  <p
    class="text-slate-600 text-center text-lg mb-16 font-['Work_Sans'] font-medium"
  >
    Chat e estatísticas em tempo real para torcer e acompanhar
  </p>
  <div class="flex flex-col items-center md:flex-row">
    <Button cssId="button-hero" href="http://" style="filled"
      >Conheça os times</Button
    >
    <Button href="http://" style="outline">Mostre sua torcida</Button>
  </div>
</section>

<style>
  section {
    background-image: url("/assets/background-pattern.png");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }
</style>
