<script>
  import "../index.css";
</script>

<div
  class="bg-gray-100 dark:bg-gray-900 dark:text-white text-gray-600 h-screen flex overflow-hidden text-sm"
>
  <slot />
</div>

<style lang="postcss">
  /* :global(html) {
    background-color: theme(colors.gray.100);
  } */
</style>
