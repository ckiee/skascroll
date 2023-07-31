<script>
  export let dir; // no type inference across components ): or files at all?

  let timeout; // key repeat wait
  let interval; // key repeat repeating

  function click() {
    window.scrollBy(
      window.innerWidth * dir.offset[0],
      window.innerHeight * dir.offset[1],
    );
  }

  function touchStart() {
    // touchStart -> touchEnd is not guaranteed, as the user may have multiple fingers
    touchEnd();
    timeout = setTimeout(() => {
      interval = setInterval(click, 400);
    }, 200);
    // TODO(config): ^ two hardcoded ms values
  }

  function touchEnd() {
    clearInterval(interval);
    clearTimeout(timeout);
  }
</script>

<button
  class="up before:content-['{dir.symbol}']
         flex-1 text-2xl border-none bg-fuchsia-400 active:bg-fuchsia-500"
  aria-label="Move page {dir.word}"
  on:click|preventDefault={click}
  on:touchstart={touchStart}
  on:touchend={touchEnd}
/>
