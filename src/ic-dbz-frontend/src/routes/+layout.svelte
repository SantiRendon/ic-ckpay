<script>
  import "../index.css";
  import Navbar from "$lib/components/Navbar.svelte";
  import Sidebar from "$lib/components/Sidebar.svelte";
  import { UserList } from "$lib/components/user";
</script>

<div
  class="bg-gray-100 dark:bg-gray-900 dark:text-white text-gray-600 h-screen flex overflow-hidden text-sm"
>
  <Sidebar />

  <div class="flex-grow overflow-hidden h-full flex flex-col">
    <Navbar />

    <!-- Content -->
    <div class="flex-grow flex overflow-x-hidden">
      <!-- UserList -->
      <UserList />

      <!-- ActivityPanel -->
      <div class="flex-grow bg-white dark:bg-gray-900 overflow-y-auto">
        <slot />
      </div>
    </div>
  </div>
</div>

<style lang="postcss">
  /* :global(html) {
    background-color: theme(colors.gray.100);
  } */
</style>
