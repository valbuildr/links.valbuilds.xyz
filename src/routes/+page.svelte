<script>
  import {
    MastodonSolid,
    BlueskySolid,
    TikTokSolid,
    SteamSolid,
    PronounsPageSolid,
    TwitchSolid,
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
  <a
    href="/youtube"
    class="flex gap-2 items-center p-2 border border-mint hover:bg-mint hover:text-black hover:fill-black"
    target="_blank"
  >
    <YoutubeSolid />
    <p>Youtube</p>
  </a>

  <a
    href="/discord"
    class="flex gap-2 items-center p-2 border border-mint hover:bg-mint hover:text-black hover:fill-black"
    target="_blank"
  >
    <DiscordSolid />
    <p>Discord</p>
  </a>

  <a
    href="/bluesky"
    class="flex gap-2 items-center p-2 border border-mint hover:bg-mint hover:text-black hover:fill-black"
    target="_blank"
  >
    <BlueskySolid />
    <p>Bluesky</p>
  </a>

  <a
    href="/mastodon"
    class="flex gap-2 items-center p-2 border border-mint hover:bg-mint hover:text-black hover:fill-black"
    target="_blank"
  >
    <MastodonSolid />
    <p>Mastodon/Fedi</p>
  </a>

  <a
    href="/github"
    class="flex gap-2 items-center p-2 border border-mint hover:bg-mint hover:text-black hover:fill-black"
    target="_blank"
  >
    <GithubSolid />
    <p>Github</p>
  </a>

  <a
    href="/tiktok"
    class="flex gap-2 items-center p-2 border border-mint hover:bg-mint hover:text-black hover:fill-black"
    target="_blank"
  >
    <TikTokSolid />
    <p>TikTok</p>
  </a>

  <a
    href="/steam"
    class="flex gap-2 items-center p-2 border border-mint hover:bg-mint hover:text-black hover:fill-black"
    target="_blank"
  >
    <SteamSolid />
    <p>Steam</p>
  </a>

  <a
    href="/pronounspage"
    class="flex gap-2 items-center p-2 border border-mint hover:bg-mint hover:text-black hover:fill-black"
    target="_blank"
  >
    <PronounsPageSolid />
    <p>Pronouns.page</p>
  </a>

  <a
    href="/twitch"
    class="flex gap-2 items-center p-2 border border-mint hover:bg-mint hover:text-black hover:fill-black"
    target="_blank"
  >
    <TwitchSolid />
    <p>Twitch</p>
  </a>

  <div
    class="flex gap-2 items-center p-2 border lg:col-span-3 border-gray-500 dark:border-gray-400 fill-gray-500 dark:fill-gray-400 text-gray-500 dark:text-gray-400"
  >
    <GlobeSolid />
    <p>Main website (coming soon)</p>
  </div>
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
