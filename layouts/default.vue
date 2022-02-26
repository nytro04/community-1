<template>
  <div class="bg-indigo-600 h-[35vh]">
    <div class="px-8 py-5">
      <AppHeader />
      <AppNav />
      <div class="">
        <Nuxt />
        <AppFooter />
      </div>
    </div>
  </div>
</template>

<script>
import AppHeader from '~/components/layout/appHeader.vue'
import AppNav from '~/components/layout/appNav.vue'
import AppFooter from '~/components/layout/appFooter.vue'
export default {
  components: { AppHeader, AppNav, AppFooter },
}
</script>

<style></style>

15077
