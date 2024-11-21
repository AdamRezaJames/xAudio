<script>
  import { onMount } from "svelte";

  let somethingState = $state(1); //state biasa
  let derivedState = $derived(somethingState * 2); // derviedState bakal update kalau somethingState berubah

  $effect(() => {
    console.log("somethingState", somethingState);
  }); //effect bakal dijalankan kalau ada perubahan pada somethingState

  onMount(() => {
    console.log("onMount");
  }); //useEffect (jalan sekali init render)
</script>

<div>
  derived State: {derivedState}
  <button onclick={() => (somethingState += 1)} class="border border-red-500"
    >BUTTON ADD</button
  >
</div>
