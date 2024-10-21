<head>
    <!-- title, description, and image for embeds -->
    <title>valentine's links</title>
    <meta name="og:title" content="valentine's links" />
    <meta name="twitter:card" content="/linksvalbuildsxyz.png" />
</head>

<script>
    import { MastodonSolid, BlueskySolid, TikTokSolid, SteamSolid, PronounsPageSolid, TwitchSolid } from '$lib';
    import { Card, Avatar, Button, Alert } from 'flowbite-svelte';
    import { YoutubeSolid, DiscordSolid, GithubSolid, GlobeSolid, TwitterSolid } from 'flowbite-svelte-icons';
</script>

<Alert color="blue" class="w-full max-w-sm">
    <span class="font-bold">You're viewing a beta layout.</span>
    This layout isn't final and is likely to change.<br />
    To go back to the main layout, <a href="/" class="hover:underline">click here</a>.
</Alert>

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

<div class="gap-3 flex flex-col w-full max-w-sm">
    <Button color="light" title="Youtube Channel" href="/youtube" target="_blank" class="hover:text-[#FF0000] hover:transition-colors duration-300">
        <div class="grid grid-cols-5 gap-3 w-full items-center">
            <YoutubeSolid class="w-6 h-6" />
            <div class="col-span-4 text-gray-500 dark:text-gray-100">
                <p>Youtube Channel</p>
            </div>
        </div>
    </Button>
    <Button color="light" title="Discord Server" href="/discord" target="_blank" class="hover:text-[#5865F2] hover:transition-colors duration-300">
        <div class="grid grid-cols-5 gap-3 w-full items-center">
            <DiscordSolid class="w-6 h-6" />
            <div class="col-span-4 text-gray-500 dark:text-gray-100">
                <p>Discord Server</p>
            </div>
        </div>
    </Button>
    <Button color="light" title="Bluesky Profile" href="/bluesky" target="_blank" class="hover:text-[#1185fE] hover:transition-colors duration-300">
        <div class="grid grid-cols-5 gap-3 w-full items-center">
            <BlueskySolid class="w-6 h-6" />
            <div class="col-span-4 text-gray-500 dark:text-gray-100">
                <p>Bluesky Profile</p>
            </div>
        </div>
    </Button>
    <Button color="light" title="Mastodon/Fedi Profile" href="/fedi" target="_blank" class="hover:text-[#6364FF] hover:transition-colors duration-300">
        <div class="grid grid-cols-5 gap-3 w-full items-center">
            <MastodonSolid class="w-6 h-6" />
            <div class="col-span-4 text-gray-500 dark:text-gray-100">
                <p>Mastodon/Fedi Profile</p>
            </div>
        </div>
    </Button>
    <Button color="light" title="Github Profile" href="/github" target="_blank" class="hover:light:text-[#1A1F24] hover:transition-colors duration-300">
        <div class="grid grid-cols-5 gap-3 w-full items-center">
            <GithubSolid class="w-6 h-6" />
            <div class="col-span-4 text-gray-500 dark:text-gray-100">
                <p>Github Profile</p>
            </div>
        </div>
    </Button>
    <Button color="light" title="TikTok Profile" href="/tiktok" target="_blank" class="hover:transition-colors duration-300">
        <div class="grid grid-cols-5 gap-3 w-full items-center">
            <TikTokSolid class="w-6 h-6" />
            <div class="col-span-4 text-gray-500 dark:text-gray-100">
                <p>TikTok Profile</p>
            </div>
        </div>
    </Button>
    <Button color="light" title="Steam Profile" href="/steam" target="_blank" class="hover:light:text-[#231F20] hover:transition-colors duration-300">
        <div class="grid grid-cols-5 gap-3 w-full items-center">
            <SteamSolid class="w-6 h-6" />
            <div class="col-span-4 text-gray-500 dark:text-gray-100">
                <p>Steam Profile</p>
            </div>
        </div>
    </Button>
    <Button color="light" title="pronouns.page Card (English)" href="/pronounspage" target="_blank" class="hover:text-[#c71585] hover:transition-colors duration-300">
        <div class="grid grid-cols-5 gap-3 w-full items-center">
            <PronounsPageSolid class="w-6 h-6" />
            <div class="col-span-4 text-gray-500 dark:text-gray-100">
                <p>pronouns.page Card (English)</p>
            </div>
        </div>
    </Button>
    <Button color="light" title="Twitch Channel" href="/twitch" target="_blank" class="hover:text-[#9146FF] hover:transition-colors duration-300">
        <div class="grid grid-cols-5 gap-3 w-full items-center">
            <TwitchSolid class="w-6 h-6" />
            <div class="col-span-4 text-gray-500 dark:text-gray-100">
                <p>Twitch Channel</p>
            </div>
        </div>
    </Button>
    <Button disabled color="light" title="Main Website (coming soon)" href="/" target="_blank" class="hover:text-violet-500 hover:transition-colors duration-300">
        <div class="grid grid-cols-5 gap-3 w-full items-center">
            <GlobeSolid class="w-6 h-6" />
            <div class="col-span-4 text-gray-500 dark:text-gray-100">
                <p>Main Website (coming soon)</p>
            </div>
        </div>
    </Button>
</div>