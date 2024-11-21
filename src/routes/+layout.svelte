<script lang="ts">
  import "../app.css";
  let { children } = $props();
  import Sidebar from "@/lib/components/Sidebar.svelte";
</script>

{@render children?.()}
<Sidebar />
