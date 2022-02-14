<script>
  import InputTable from "./InputTable.svelte";

  let trackWidth = 100;
  let fabricWidth = 148;

  let finishedLength = 200;
  let hems = 15;

  $: totalLength = finishedLength + hems;
  $: drops = fabricWidth / trackWidth;
  $: fabricNeeded = drops * totalLength;
  $: fulnessAchieved = trackWidth / drops;
</script>

<div
  class="relative flex flex-col min-w-0 break-words bg-white w-full mb-6 shadow-lg rounded"
>
  <div class="rounded-t mb-0 px-4 py-3 border-0">
    <div class="flex flex-wrap items-center">
      <div class="relative w-full px-4 max-w-full flex-grow flex-1">
        <h3 class="font-semibold text-base text-blueGray-700">
          Social traffic
        </h3>
      </div>
      <div class="relative w-full px-4 max-w-full flex-grow flex-1 text-right">
        <button
          class="bg-indigo-500 text-white active:bg-indigo-600 text-xs font-bold uppercase px-3 py-1 rounded outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150"
          type="button"
        >
          See all
        </button>
      </div>
    </div>
  </div>
  <InputTable />
</div>
