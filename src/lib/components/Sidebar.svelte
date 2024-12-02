<script lang="ts">
  // import { onMount } from "svelte";

  // let somethingState = $state(1); //state biasa
  // let derivedState = $derived(somethingState * 2); // derviedState bakal update kalau somethingState berubah

  // $effect(() => {
  //   console.log("somethingState", somethingState);
  // }); //effect bakal dijalankan kalau ada perubahan pada somethingState

  // onMount(() => {
  //   console.log("onMount");
  // }); //useEffect (jalan sekali init render)

  import { Menu, House, Library, Plus, Pin, CirclePlay } from "lucide-svelte";
  import Separator from "./ui/separator/separator.svelte";
  import Button from "./ui/button/button.svelte";
  import ScrollArea from "./ui/scroll-area/scroll-area.svelte";
  import { cn } from "../utils";

  const sidebarContent = [
    {
      name: "Home",
      icon: House,
    },
    {
      name: "Library",
      icon: Library,
    },
  ];

  const playlists = [
    {
      name: "Playlist 1",
      desc: "Lyvera",
    },
    {
      name: "Playlist 2",
      desc: "Lyvera",
    },
    {
      name: "Playlist 3",
      desc: "Lyvera",
    },
    {
      name: "Playlist 4",
      desc: "Lyvera",
    },
    {
      name: "Playlist 5",
      desc: "Lyvera",
    },
    {
      name: "Playlist 6",
      desc: "Lyvera",
    },
    {
      name: "Playlist 7",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
    {
      name: "Playlist 8",
      desc: "Lyvera",
    },
  ];

  let hoverTrue = $state<boolean[]>([]);
  let focusTrue = $state<boolean[]>([]);
</script>

<div class="p-4 flex-col flex w-[12vw] h-screen gap-6 border-r">
  <div class="flex w-full h-fit gap-6 items-center">
    <Menu
      size={25}
      class="hover:bg-neutral-400 rounded-full transition ease-in-out"
    />
    <p class="text-lg">xAudio</p>
  </div>
  <div class="flex flex-col w-full gap-2">
    {#each sidebarContent as cont}
      <div
        class="flex w-full gap-4 items-center rounded-xl hover:bg-neutral-400 p-2 transition ease-in-out"
      >
        {#key cont.icon}
          <cont.icon size={20} />
          <p class="text-lg">{cont.name}</p>
        {/key}
      </div>
    {/each}
  </div>
  <Separator class="w-full" />

  <div class="flex flex-col w-full h-full gap-2">
    <Button
      class="flex gap-2 items-center justify-start rounded-xl"
      variant="secondary"
    >
      <Plus />
      <p class="text-lg">New Playlist</p>
    </Button>
    <ScrollArea class="w-full h-[75vh]">
      <div
        class="flex flex-col w-full py-2 pl-2 hover:bg-neutral-700/50 rounded-xl justify-center"
      >
        <p>Liked Music</p>
        <div class="flex text-xs items-center">
          <Pin size={15} />
          <p class="pl-1">Auto Playlist</p>
        </div>
      </div>
      {#each playlists as playlist, i}
        <div
          class="flex w-full py-2 pl-2 hover:bg-neutral-700/50 rounded-xl"
          onmouseover={() => (hoverTrue[i] = true)}
          onmouseleave={() => (hoverTrue[i] = false)}
          onfocus={() => (focusTrue[i] = true)}
          role="button"
          tabindex="0"
        >
          <div class="flex flex-col w-full justify-between">
            <p>{playlist.name}</p>
            <div class="flex gap-2 text-xs items-center">
              <p>{playlist.desc}</p>
            </div>
          </div>
          <div class="pr-6 items-center flex">
            <CirclePlay size={23} class={cn(hoverTrue[i] ? "" : "hidden")} />
          </div>
        </div>
      {/each}
    </ScrollArea>
  </div>
</div>
