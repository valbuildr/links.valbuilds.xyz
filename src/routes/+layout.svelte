<script>
    import "../app.css";
    import { DarkMode } from 'flowbite-svelte';
</script>

<head>
    <!-- google fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Instrument+Sans:ital,wght@0,400..700;1,400..700&display=swap" rel="stylesheet" />
    <!-- apple touch icon -->
    <link rel="apple-touch-icon" sizes="57x57" href="/apple-touch-icon-57.png" />
    <link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon-180.png" />
</head>

<div class="flex flex-col min-h-screen dark:bg-slate-700">
    <div class="flex flex-col p-3 items-end">
        <DarkMode />
    </div>
    <div class="flex flex-col flex-1 p-3 items-center place-content-center gap-3 h-full">
        <slot />
    </div>
    <!-- <footer class="bg-gray-200 dark:bg-slate-800 p-3">
        <h3 class="text-lg dark:text-white">Made with ❤️ by valbuilded.</h3>
    </footer> -->
</div>
