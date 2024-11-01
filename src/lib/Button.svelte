<script lang="ts">
  export let href: string;
</script>

<a
  {href}
  class="flex gap-2 items-center p-2 border border-dark-mint dark:border-mint hover:bg-dark-mint dark:hover:bg-mint hover:text-white hover:fill-white hover:dark:text-black hover:dark:fill-black"
  target="_blank"
>
  <slot />
</a>
