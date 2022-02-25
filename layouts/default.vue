<template>
  <div class="bg-indigo-600">
    <div class="px-8 py-5">
      <AppHeader />
      <AppNav />

      <Nuxt />
    </div>
  </div>
</template>

<script>
import AppHeader from '~/components/layout/appHeader.vue'
import AppNav from '~/components/layout/appNav.vue'
export default {
  components: { AppHeader, AppNav },
}
</script>

<style></style>

15077
