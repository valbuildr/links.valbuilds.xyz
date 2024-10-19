<head>
    <!-- title, description, and image for embeds -->
    <title>valentine's links</title>
    <meta name="og:description" content="valbuildr's official platforms." />
    <meta name="og:image" content="/linksvalbuildsxyz.png" />
    <!-- google fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Instrument+Sans:ital,wght@0,400..700;1,400..700&display=swap" rel="stylesheet" />
    <!-- apple touch icon -->
    <link rel="apple-touch-icon" sizes="57x57" href="/apple-touch-icon-57.png" />
    <link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon-180.png" />
</head>

<script>
    import { MastodonSolid, BlueskySolid, TikTokSolid, SteamSolid, PronounsPageSolid, TwitchSolid } from '$lib';
    import { Card, Avatar, Button, Alert } from 'flowbite-svelte';
    import { YoutubeSolid, DiscordSolid, GithubSolid, GlobeSolid, TwitterSolid } from 'flowbite-svelte-icons';
</script>

<Card img="/banner.png" padding="md">
    <div class="flex flex-col items-start pb-4">
        <Avatar size="lg" src="/pfp.png" />
        <h5 class="mt-2 text-xl font-medium text-gray-900 dark:text-white">Valentine</h5>
        <h6 class="text-md font-semibold text-gray-700 dark:text-gray-300">valbuildr • <a href="https://en.pronouns.page/@valbuilded" title="Click to go to my pronouns.page card.">she/they</a></h6>
        <span class="mt-1 text-sm text-gray-500 dark:text-gray-100">a person that makes things on the internet sometimes.<br /><br /><i>banner by <a href="https://starsleeps.carrd.co/" class="hover:underline">starsleeps</a></i></span>
    </div>
</Card>

<Alert color="yellow" class="w-full max-w-sm">
    <TwitterSolid slot="icon" class="w-5 h-5" />
    <span class="font-bold">I no longer use Twitter!</span>
    Any account claiming to be me on Twitter is fake, do not interact wth them.<br />
</Alert>

<div class="grid grid-cols-5 gap-3 w-full max-w-sm">
    <Button color="light" href="https://www.youtube.com/@valbuildr" class="hover:text-[#FF0000] hover:transition-colors duration-300"><YoutubeSolid class="w-6 h-6" /></Button>
    <Button color="light" href="https://discord.gg/UKVMvUG2h9" class="hover:text-[#5865F2] hover:transition-colors duration-300"><DiscordSolid class="w-6 h-6" /></Button>
    <Button color="light" href="https://bsky.app/profile/valbuilds.xyz" class="hover:text-[#1185fE] hover:transition-colors duration-300"><BlueskySolid class="w-6 h-6" /></Button>
    <Button color="light" href="https://wetdry.world/@valbuildr" class="hover:text-[#6364FF] hover:transition-colors duration-300"><MastodonSolid class="w-6 h-6" /></Button>
    <Button color="light" href="https://github.com/valbuildr" class="hover:light:text-[#1A1F24] hover:transition-colors duration-300"><GithubSolid class="w-6 h-6" /></Button>

    <Button color="light" href="https://tiktok.com/@valbuildr" class="hover:transition-colors duration-300"><TikTokSolid class="w-6 h-6" /></Button>
    <Button color="light" href="https://steamcommunity.com/id/valbuilds" class="hover:light:text-[#231F20] hover:transition-colors duration-300"><SteamSolid class="w-6 h-6" /></Button>
    <Button color="light" href="https://en.pronouns.page/@valbuilded" class="hover:text-[#c71585] hover:transition-colors duration-300"><PronounsPageSolid class="w-6 h-6" /></Button>
    <Button color="light" href="https://www.twitch.tv/valbuildr" class="hover:text-[#9146FF] hover:transition-colors duration-300"><TwitchSolid class="w-6 h-6" /></Button>
    <Button color="light" href="https://www.valbuilds.xyz/" disabled class="hover:text-violet-500 hover:transition-colors duration-300"><GlobeSolid class="w-6 h-6" /></Button>
</div>