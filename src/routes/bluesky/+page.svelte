<script>
  const url = "https://bsky.app/profile/valbuilds.xyz";

  import { browser } from "$app/environment";

  if (browser) {
    window.location.href = url;
  }
</script>

<head>
  <!-- title, description, and image for embeds -->
  <title>valentine's bluesky</title>
  <meta name="og:title" content="valentine's bluesky" />
  <meta name="twitter:card" content="/linksvalbuildsxyz.png" />
</head>

<div class="text-center">
  <h5 class="mt-2 text-xl font-medium text-black dark:text-white pb-2">
    Redirecting...
  </h5>
  <h6 class="text-md text-gray-500 dark:text-gray-400">
    If it isn't working, click <a href={url} class="hover:underline">here</a>.
  </h6>
</div>
