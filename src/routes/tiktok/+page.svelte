<script>
    const url = "https://tiktok.com/@valbuildr";

    import { browser } from '$app/environment';
    
    if (browser) {
        window.location.href = url;
    }

    import { Spinner } from "flowbite-svelte";
</script>

<head>
    <!-- title, description, and image for embeds -->
    <title>valentine's tiktok</title>
    <meta name="og:title" content="valentine's tiktok" />
    <meta name="og:image" content="/linksvalbuildsxyz.png" />
</head>

<div class="text-center">
    <h5 class="mt-2 text-xl font-medium text-gray-900 dark:text-white pb-2">Redirecting...</h5>
    <Spinner size={8} />
    <h6 class="text-md text-gray-700 dark:text-gray-300">If it isn't working, click <a href={url} class="hover:underline">here</a>.</h6>
</div>