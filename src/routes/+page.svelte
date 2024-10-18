<head>
    <title>valentine's links</title>
    <meta name="og:description" content="valbuildr's official platforms." />
    <meta name="og:image" content="/linksvalbuildsxyz.png" />
</head>

<script>
    // import MastodonSolid from '$lib/MastodonSolid.svelte';
    // import BlueskySolid from '$lib/BlueskySolid.svelte';
    // import TikTokSolid from '$lib/TikTokSolid.svelte';
    import { MastodonSolid, BlueskySolid, TikTokSolid } from '$lib';
    import { Card, Avatar, Button, Alert } from 'flowbite-svelte';
    import { YoutubeSolid, DiscordSolid, GithubSolid } from 'flowbite-svelte-icons';
  </script>

<Alert color="yellow" class="text-center w-full max-w-sm">
    <span class="font-medium">I no longer use Twitter!</span>
    Any account claiming to be me on Twitter is fake, do not interact wth them.<br />
    <span class="text-gray-700 dark:text-gray-300">The platforms linked below are my official ones. :)</span>
</Alert>

<Card img="/banner.png" padding="md">
    <div class="flex flex-col items-start pb-4">
        <Avatar size="lg" src="/pfp.png" />
        <h5 class="mt-2 text-xl font-medium text-gray-900 dark:text-white">Valentine</h5>
        <h6 class="text-md font-semibold text-gray-700 dark:text-gray-300">valbuildr • she/they</h6>
        <span class="mt-1 text-sm text-gray-500 dark:text-gray-100">a person that makes things on the internet sometimes.<br /><br /><i>banner by <a href="https://starsleeps.carrd.co/" class="hover:underline">starsleeps</a></i></span>
    </div>
</Card>

<div class="grid grid-cols-5 gap-3">
    <Button color="light" href="https://www.youtube.com/@valbuildr"><YoutubeSolid class="w-6 h-6" /></Button>
    <Button color="light" href="https://discord.gg/UKVMvUG2h9"><DiscordSolid class="w-6 h-6" /></Button>
    <Button color="light" href="https://bsky.app/profile/valbuilds.xyz"><BlueskySolid class="w-6 h-6" /></Button>
    <Button color="light" href="https://wetdry.world/@valbuildr"><MastodonSolid class="w-6 h-6" /></Button>
    <Button color="light" href="https://github.com/valbuildr"><GithubSolid class="w-6 h-6" /></Button>
    <Button color="light" href="/more" class="col-span-5"><TikTokSolid class="w-6 h-6" /></Button>
</div>