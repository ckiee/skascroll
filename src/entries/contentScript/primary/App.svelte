<script lang="ts">
  import "~/index.css";
  import NavigationButton from "./NavigationButton.svelte";

  // package for this? 🥺
  const directions = [
    { word: "up", symbol: "↑", offset: [0, -1] },
    { word: "down", symbol: "↓", offset: [0, 1] },
  ];

  // TODO: disable scrolling when the user is interacting with our overlay
</script>

<!-- TODO: root text-[16px] should be customizable, it's there because
     we can't rely on host page rem to always be default -->
<div
  class="z-[999991312]
         fixed bottom-[2vh] right-[2vh] w-16 h-48 text-[16px]
         opacity-80 bg-fuchsia-800
         flex flex-col gap-1 p-1 rounded"
  aria-label="skascroll navigation overlay"
>
  {#each directions as dir}
    <NavigationButton {dir} />
  {/each}
  <span class="text-center">🐈</span>
</div>
