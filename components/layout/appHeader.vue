<template>
  <div class="">
    <div class="flex items-center justify-between pb-5 space-x-4 lg:space-x-0">
      <span class="text-gray-100 material-icons"> home </span>

      <div class="relative lg:hidden">
        <span class="absolute text-gray-300 material-icons left-3 top-[10px]">
          search
        </span>
        <input
          type="text"
          v-model="search"
          placeholder="Search"
          class="w-full pl-10 text-lg text-gray-300 bg-indigo-500 border-none rounded-md placeholder:text-gray-300"
        />
      </div>
      <div class="-my-2 lg:hidden">
        <button
          @click="() => (open = true)"
          type="button"
          class="inline-flex items-center justify-center p-2 text-gray-400 hover:text-gray-500"
          aria-expanded="false"
        >
          <span class="sr-only">Open menu</span>
          <span class="text-gray-100 material-icons"> menu </span>
        </button>
      </div>
      <div class="items-center hidden space-x-4 lg:flex">
        <span class="text-gray-100 material-icons"> notifications </span>
        <img
          class="w-8 h-8 rounded-full"
          :src="require(`~/assets/images/${profileImg}.png`)"
          alt=""
        />
      </div>

      <div
        class="absolute inset-x-0 z-10 p-2 transition origin-top-right transform top-2 right-4 md:hidden"
        v-if="open"
      >
        <div
          class="bg-white divide-y-2 rounded-lg shadow-md ring-1 ring-black ring-opacity-5 divide-gray-50"
        >
          <div class="p-5">
            <div class="flex items-center justify-between">
              <div class="flex justify-start lg:w-0 lg:flex-1">
                <nuxt-link to="/" class="flex space-x-2">
                  <span class="text-gray-500 material-icons"> home </span>
                </nuxt-link>
              </div>
              <div class="-mr-2">
                <button
                  @click="() => (open = false)"
                  type="button"
                  class="inline-flex items-center justify-center p-2 text-gray-400 bg-white rounded-md hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500"
                >
                  <span class="sr-only">Close menu</span>
                  <span class="material-icons-outlined"> close </span>
                </button>
              </div>
            </div>
          </div>
          <ul class="px-5 py-6 space-y-6">
            <li
              v-for="nav in navs"
              :key="nav.name"
              class="flex flex-col space-y-8"
            >
              <nuxt-link
                :to="nav.url"
                class="text-lg font-semibold text-gray-500 font-gotham whitespace-nowrap hover:text-gray-900"
              >
                {{ nav.name }}
              </nuxt-link>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <AppNav :navs="navs" />
  </div>
</template>

<script>
import AppNav from './appNav.vue'
export default {
  data: () => ({
    search: '',
    open: false,
    profileImg: 'stef',
    navs: [
      { name: 'Home', url: '#' },
      { name: 'Profile', url: '#' },
      { name: 'Resources', url: '#' },
      { name: 'Company Directory', url: '#' },
      { name: 'Openings', url: '#' },
    ],
  }),
  watch: {
    $route(newRoute, oldRoute) {
      if (newRoute) {
        this.open = false
      }
    },
  },
  components: { AppNav },
}
</script>

<style lang="css" scoped>
.header-bg {
  background: linear-gradient(
    0deg,
    rgba(255, 255, 255, 1) 0%,
    rgba(241, 245, 249, 1) 32%
  );
}
</style>
