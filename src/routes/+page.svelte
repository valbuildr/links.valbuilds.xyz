<script>
  import {
    MastodonSolid,
    BlueskySolid,
    TikTokSolid,
    SteamSolid,
    PronounsPageSolid,
    TwitchSolid,
    Button,
  } from "$lib";
  import {
    YoutubeSolid,
    DiscordSolid,
    GithubSolid,
    GlobeSolid,
    TwitterSolid,
  } from "flowbite-svelte-icons";

  let bio = "a person that makes things on the internet sometimes.";

  // profile picture by _____.
  let pfpCreditText = "✦絢瀬 on picrew";
  let pfpCreditLink = "https://picrew.me/en/image_maker/1904634";
</script>

<head>
  <!-- title, description, and image for embeds -->
  <title>valentine's links</title>
  <meta name="og:title" content="valentine's links" />
  <meta name="twitter:card" content="/linksvalbuildsxyz.png" />
</head>

<div class="flex gap-3 items-center">
  <img
    class="sm:w-24 sm:h-24 w-20 h-20 mb-3 rounded-full shadow-lg"
    src="/pfp.png"
    alt="Profile"
  />
  <div class="flex flex-col gap-2">
    <h3 class="sm:text-3xl text-2xl font-bold">Valentine</h3>
    <h5 class="sm:text-xl text-md text-gray-500 dark:text-gray-400">
      valbuildr • <a href="/pronounspage" class="hover:underline">she/they</a>
    </h5>
  </div>
</div>

<p>
  {bio}
  {#if pfpCreditText}
    <br /><br />profile picture by
    <a class="hover:underline" href={pfpCreditLink}>{pfpCreditText}</a>.
  {/if}
</p>

<hr class="my-2 border-gray-500 dark:border-gray-400" />

<div class="flex flex-col md:grid md:grid-cols-2 lg:grid-cols-3 gap-2">
  <Button href="/youtube">
    <YoutubeSolid />
    <p>Youtube</p>
  </Button>

  <Button href="/discord">
    <DiscordSolid />
    <p>Discord</p>
  </Button>

  <Button href="/bluesky">
    <BlueskySolid />
    <p>Bluesky</p>
  </Button>

  <Button href="/mastodon">
    <MastodonSolid />
    <p>Mastodon/Fedi</p>
  </Button>

  <Button href="/github">
    <GithubSolid />
    <p>Github</p>
  </Button>

  <Button href="/tiktok">
    <TikTokSolid />
    <p>TikTok</p>
  </Button>

  <Button href="/steam">
    <SteamSolid />
    <p>Steam</p>
  </Button>

  <Button href="/pronounspage">
    <PronounsPageSolid />
    <p>Pronouns.page (English)</p>
  </Button>

  <Button href="/twitch">
    <TwitchSolid />
    <p>Twitch</p>
  </Button>

  <a
    class="flex gap-2 items-center p-2 border border-dark-mint dark:border-mint hover:bg-dark-mint dark:hover:bg-mint hover:text-white hover:fill-white hover:dark:text-black hover:dark:fill-black lg:col-span-3"
    href="https://www.valbuilds.xyz"
    target="_blank"
  >
    <GlobeSolid />
    <p>Main website</p>
  </a>
</div>

<hr class="my-2 border-gray-500 dark:border-gray-400" />

<div
  class="flex gap-2 items-center p-2 border border-yellow-500 dark:border-yellow-400 fill-yellow-500 dark:fill-yellow-400 text-yellow-500 dark:text-yellow-400"
>
  <TwitterSolid />
  <p>
    <span class="font-bold">I no longer use Twitter!</span>
    Any account claiming to be me on Twitter is fake, do not interact wth them.
  </p>
</div>
