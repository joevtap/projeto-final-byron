<script>
  import { Link } from "svelte-routing";

  const src = "assets/Logo.svg";
  let isNavOpen = false;
  export let type = "home"; // home or back
  export let color = "text-white";

  function toggleNav() {
    isNavOpen = !isNavOpen;
  }
</script>

{#if type == "home"}
  <nav
    class="bg-white/25 fixed z-10 w-full flex items-center justify-between px-16 h-16"
  >
    <img class="w-12 object-contain" {src} alt="League of Byron" />
    <ul class="flex flex-wrap items-center" class:nav-open={isNavOpen}>
      <li class="text-slate-700 hover:text-slate-500 py-2 mr-14">
        <a href="#mostre-sua-torcida" on:click={toggleNav}>Mostre sua torcida</a
        >
      </li>
      <li class="text-slate-700 hover:text-slate-500 py-2">
        <a href="#times" on:click={toggleNav}>Times</a>
      </li>
    </ul>
    <button on:click={toggleNav} class="p-2 text-slate-700">Menu</button>
  </nav>
{:else}
  <nav
    class="bg-transparent fixed z-10 w-full flex items-center justify-start px-16 h-16"
  >
    <Link class="hover:brightness-110 py-2 {color}" to="/">Home</Link>
  </nav>
{/if}

<style>
  nav {
    backdrop-filter: blur(8px);
    box-shadow: 0px 12px 40px -12px rgba(51, 65, 85, 0.08);
    opacity: 0;
    transform: translateY(-100%);
    animation: fade forwards 300ms ease-out 300ms;
  }

  button {
    display: none;
  }

  @media screen and (max-width: 768px) {
    button {
      display: block;
    }

    nav ul {
      position: fixed;
      top: 0;
      left: 0;
      background: #fff;
      width: 100vw;
      height: 100vh;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      z-index: 9;
      margin-top: 100%;
      padding-bottom: 56px;
      opacity: 0;
      pointer-events: none;

      transition: 150ms;
    }

    nav ul li {
      margin: 2rem 0;
    }

    nav ul li a {
      font-size: 1.2rem;
    }

    .nav-open {
      opacity: 1;
      pointer-events: all;
      margin-top: 56px;
    }
  }

  @keyframes fade {
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>
