<script>
    import MastodonSolid from '$lib/MastodonSolid.svelte';
    import { Card, Avatar, Button, Popover } from 'flowbite-svelte';
    import { TwitterSolid, YoutubeSolid, DiscordSolid, GithubSolid } from 'flowbite-svelte-icons';
  </script>

<Card img="/banner.png" padding="md">
    <div class="flex flex-col items-start pb-4">
        <Avatar size="lg" src="/pfp.png" />
        <h5 class="mt-2 mb-1 text-xl font-medium text-gray-900 dark:text-white">valbuildr</h5>
        <span class="text-sm text-gray-500 dark:text-gray-400">a person that makes things on the internet sometimes.<br /><br /><i>banner by <a href="https://twitter.com/starsleeps" class="hover:underline">starsleeps</a></i></span>
    </div>
</Card>

<div class="grid grid-cols-5 gap-3">
    <Button color="light" href="https://twitter.com/valonthenet"><TwitterSolid class="w-6 h-6" /></Button>
    <Button color="light" href="https://www.youtube.com/@valbuildr"><YoutubeSolid class="w-6 h-6" /></Button>
    <Button color="light" href="https://discord.gg/UKVMvUG2h9"><DiscordSolid class="w-6 h-6" /></Button>
    <Button id="mastodonbutton" color="light" href="https://wetdry.world/@valbuildr"><MastodonSolid class="w-6 h-6" /></Button>
    <Button color="light" href="https://github.com/valbuildr"><GithubSolid class="w-6 h-6" /></Button>

    <!-- <Button color="light" href="/more" class="col-span-5">See more</Button> -->
</div>

<Popover class="w-64 text-sm font-light" title="This is supposed to be the Mastodon logo." triggeredBy="#mastodonbutton">But I can't seem to get the icon to work. If you have a fix, please do get in touch.<br />Click the button to visit my profile on the Fediverse.</Popover>