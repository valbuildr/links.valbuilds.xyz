<script>
    import "../app.css";
    import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, DarkMode } from 'flowbite-svelte';
</script>

<div class="flex flex-col min-h-screen dark:bg-slate-700">
    <div class="flex flex-col p-3 items-end">
        <DarkMode />
    </div>
    <div class="flex flex-col flex-1 p-3 items-center place-content-center gap-3 h-full">
        <slot />
    </div>
    <footer class="bg-gray-200 dark:bg-slate-800 p-3">
        <h3 class="text-lg dark:text-white">Made with ❤️ by valbuilded.</h3>
    </footer>
</div>
