<script>
  import "../app.css";
  import { DarkMode } from "flowbite-svelte";
</script>

<div
  class="bg-white dark:bg-gray-800 text-black dark:text-white font-mono min-h-screen"
>
  <nav
    class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4 text-black"
  >
    <a href="/" class="flex items-center space-x-3 rtl:space-x-reverse">
      <span class="bg-mint p-3 font-mono font-bold sm:text-xl text-md"
        >links.valbuilds.xyz</span
      >
    </a>
    <div class="w-auto" id="navbar-default">
      <DarkMode />
    </div>
  </nav>
  <div class="flex flex-col flex-1 max-w-screen-xl mx-auto p-4">
    <slot />
  </div>
</div>
