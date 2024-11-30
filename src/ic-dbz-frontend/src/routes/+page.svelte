<script>
  import {
    ActivityFilters,
    ActivityTable,
    ActivityTableFooter,
  } from "$lib/components/activity";
  import { UserInfo } from "$lib/components/user";
</script>

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
