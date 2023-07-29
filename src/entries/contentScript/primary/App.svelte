<script lang="ts">
 import "~/index.css";
  // import logo from "~/assets/logo.svg";
  //
  // const logoImageUrl = new URL(logo, import.meta.url).href;
  function s(pages: number) {
    window.scrollBy(0, pages * window.innerHeight);
  }
</script>

<div class="overlay">
  <button class="up" aria-label="Page up" on:click={() => s(-1)}></button>
  <button class="down" aria-label="Page down" on:click={() => s(1)}></button>
  🐈
</div>

<style>
  .overlay {
    z-index: 999991312;
    position: fixed;
    bottom: 20px;
    right: 10px;
    width: 64px;
    height: 128px;
    display: flex;
    flex-direction: column;
    background-color: #faf;
    opacity: 0.8;

    text-align: center;
  }

  button {
    width: 100%;
    height: 64px;
    font-size: 32px;
    border: 0;
  }

  button:hover {
    background: #fef;
  }

  .up::before {
    content: "↑";
  }
  .down::before {
    content: "↓";
  }
</style>
