<script>
  import { page } from "$app/stores";
</script>

<div class="text-center">
  <h5 class="mt-2 text-xl font-medium text-black dark:text-white pb-2">
    {$page.status}
  </h5>
  <h6 class="text-md text-gray-500 dark:text-gray-400">
    {$page.error.message}
  </h6>
</div>
