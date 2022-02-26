<script>
  export let player = {
    name: "",
    pic: "",
    role: "",
    roleImage: "",
  };
</script>

<div
  id="card-player"
  class="w-[348px] flex-grow-1 rounded-[8px] gap-4 cursor-pointer flex flex-row items-center py-6 px-10 border-[1px] border-slate-200 bg-slate-50"
>
  <img class="h-[210px]" src="{player.pic}" alt={player.name} />

  <div>
    <img src="{player.roleImage}" alt="{player.role}">
  </div>
  <div>
    <p class="text-lg font-bold text-black">{player.name}</p>
    <p class="text-sm font-normal text-slate-600">{player.role}</p>
  </div>

</div>


<style>
  #card-player {
    box-shadow: 0px 12px 24px -16px rgba(51, 65, 85, 0.16);
    transition: 300ms;
    width: 348px;
  }

  #card-player:hover {
    transform: translateY(-5px) scale(1.05);
    box-shadow: 0px 12px 24px -8px rgba(51, 65, 85, 0.16);
  }
</style>
