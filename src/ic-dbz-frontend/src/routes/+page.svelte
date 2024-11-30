<script>
  import {
    ActivityFilters,
    ActivityTable,
    ActivityTableFooter,
  } from "$lib/activity";

  import { UserInfo, UserList } from "$lib/user";

  import Navbar from "$lib/Navbar.svelte";

  import Sidebar from "$lib/Sidebar.svelte";

  import { onMount } from "svelte";

  onMount(() => {
    console.log("mount");
  });
</script>

<Sidebar />

<div class="flex-grow overflow-hidden h-full flex flex-col">
  <Navbar />

  <!-- Content -->
  <div class="flex-grow flex overflow-x-hidden">
    <!-- UserList -->
    <UserList />

    <!-- ActivityPanel -->
    <div class="flex-grow bg-white dark:bg-gray-900 overflow-y-auto">
      <!-- UserInfo -->
      <UserInfo />

      <div class="sm:p-7 p-4">
        <!-- ActivityFilters -->
        <ActivityFilters />

        <!-- ActivityTable -->
        <ActivityTable />
        <!-- ActivityTableFooter -->
        <ActivityTableFooter />
      </div>
    </div>
  </div>
</div>
