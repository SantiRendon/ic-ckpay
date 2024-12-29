<script>
  import {
    ActivityFilters,
    ActivityTable,
    ActivityTableFooter,
  } from "$lib/components/activity";
  import { UserInfo, UserList } from "$lib/components/user";
</script>

<!-- UserList -->
<UserList />

<!-- ActivityPanel -->
<div class="flex-grow bg-white dark:bg-gray-900 overflow-y-auto">
  <!-- <slot /> -->
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
