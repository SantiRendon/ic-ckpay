<script>
  import ActivityTableFooter from "$lib/ActivityTableFooter.svelte";

  import ActivityTable from "$lib/ActivityTable.svelte";

  import ActivityFilters from "$lib/ActivityFilters.svelte";

  import UserInfo from "$lib/UserInfo.svelte";

  import UserList from "$lib/UserList.svelte";

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
