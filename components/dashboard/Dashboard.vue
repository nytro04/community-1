<template>
  <div class="grid grid-cols-1 gap-x-10 md:grid-cols-3 h-[70vh] mb-8">
    <DashboardLeft />
    <DashboardRight />
  </div>
</template>

<script>
import DashboardLeft from './DashboardLeft.vue'
import DashboardRight from './DashboardRight.vue'
export default {
  components: { DashboardLeft, DashboardRight },
}
</script>

<style></style>
