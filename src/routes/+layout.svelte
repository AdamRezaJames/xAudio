<script lang="ts">
  import "../app.css";
  let { children } = $props();
  import Sidebar from "@/lib/components/Sidebar.svelte";
  import TailwindIndicator from "@/lib/components/ui/tailwind-indicator.svelte";
</script>

<div class="grid grid-cols-[auto,1fr]">
  <Sidebar />
  {@render children?.()}
</div>
<TailwindIndicator />
