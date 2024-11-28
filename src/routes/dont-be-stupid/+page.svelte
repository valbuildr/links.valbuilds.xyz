<script>
    import { page } from '$app/stores';

    const licensorSpecified = $page.url.searchParams.get('licensor');
    let licensor = "valbuildr";
    if (licensorSpecified != null) {
        licensor = licensorSpecified;
    }
</script>


<head>
    <!-- title, description, and image for embeds -->
    <title>The 'Dont be Stupid' License</title>
    <meta name="og:title" content="The 'Dont be Stupid' License" />
    <meta name="twitter:card" content="/linksvalbuildsxyz.png" />
</head>

<h3 class="sm:text-3xl text-2xl font-bold mb-4">The 'Dont be Stupid' License</h3>

<div
  class="mb-4 flex gap-2 items-center p-2 border border-yellow-500 dark:border-yellow-400 fill-yellow-500 dark:fill-yellow-400 text-yellow-500 dark:text-yellow-400"
>
  <p>
    I am not a lawyer, just a person that does things online.
    <span class="font-bold">This is not legal advice.</span>
  </p>
</div>

<p class="mb-4">You can do basically anything except be stupid or bigoted with the work under this license.</p>

<p class="mb-4">The licensor, {licensor}, holds all rights to the work, and can ask you to cease usage at any time, for any reason. (even ones not listed as prohibited under this license)</p>

<div
  class="mb-4 flex gap-2 items-center p-2 border border-blue-500 dark:border-blue-400 fill-blue-500 dark:fill-blue-400 text-blue-500 dark:text-blue-400"
>
  <p>
    <span class="font-bold">Want your own name on this license?</span>
    Add "?licensor=yourname" to the URL.
  </p>
</div>