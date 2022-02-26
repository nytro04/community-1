<template>
  <div class="min-h-screen">
    <Dashboard />
  </div>
</template>

<script>
import Dashboard from '~/components/dashboard/Dashboard.vue'
export default {
  name: 'IndexPage',
  head() {
    return {
      title: 'Home Page',
    }
  },
  components: { Dashboard },
}
</script>
