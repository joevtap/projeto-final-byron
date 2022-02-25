<script>
  import { navigate } from "svelte-routing";

  export let team = {
    name: "",
    shortName: "",
    description: "",
    image: "",
  };

  function goTo() {
    setTimeout(() => {
      navigate("/team/" + team.shortName, { replace: true });
    }, 10);
  }
</script>

<div
  id="card"
  class="flex-grow-1 rounded-[8px] gap-4 cursor-pointer flex flex-row items-center py-6 px-10 border-[1px] border-slate-200 bg-slate-50"
  data-bs-toggle="modal"
  data-bs-target={"#" + team.shortName + "modal"}
>
  <img class="w-12 h-12 object-contain" src={team.image} alt={team.name} />
  <div>
    <p class="text-lg font-bold text-slate-900">{team.name}</p>
    <p class="text-sm font-normal text-slate-600">{team.shortName}</p>
  </div>
</div>

<!-- Modal -->
<div
  class="modal fade"
  id={team.shortName + "modal"}
  tabindex="-1"
  aria-labelledby="teamModalLabel"
  aria-hidden="true"
>
  <div class="modal-dialog modal-dialog-centered">
    <div class="modal-content">
      <div class="modal-header">
        <h3 class="modal-title" id="exampleModalLabel">{team.name}</h3>
        <button
          type="button"
          class="btn-close"
          data-bs-dismiss="modal"
          aria-label="Close"
        />
      </div>
      <div class="modal-body">
        <div>
          <img src={team.image} alt={team.name} />
          <p>{team.description}</p>
        </div>
      </div>
      <div class="modal-footer">
        <a
          href={"/" + team.shortName}
          on:click={goTo}
          data-bs-dismiss="modal"
          class="block p-2 cursor-pointer text-sky-700 font-medium text-base"
          >Ver mais</a
        >
      </div>
    </div>
  </div>
</div>

<style>
  .btn-close {
    box-sizing: content-box;
    width: 1.2rem;
    height: 1.2rem;
    padding: 0.25em 0.25em;
    color: #000;
    background: transparent
      url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16' fill='%23000'%3e%3cpath d='M.293.293a1 1 0 011.414 0L8 6.586 14.293.293a1 1 0 111.414 1.414L9.414 8l6.293 6.293a1 1 0 01-1.414 1.414L8 9.414l-6.293 6.293a1 1 0 01-1.414-1.414L6.586 8 .293 1.707a1 1 0 010-1.414z'/%3e%3c/svg%3e")
      center/1em auto no-repeat;
    border: 0;
    border-radius: 0.25rem;
    opacity: 0.5;
  }

  #card {
    box-shadow: 0px 12px 24px -16px rgba(51, 65, 85, 0.16);
    transition: 300ms;
  }

  #card:hover {
    transform: translateY(-5px) scale(1.05);
    box-shadow: 0px 12px 24px -8px rgba(51, 65, 85, 0.16);
  }
</style>
