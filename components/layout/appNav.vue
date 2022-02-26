<template>
  <nav
    class="hidden grid-cols-1 py-6 border-t border-white lg:grid lg:space-x-10 border-opacity-30 md:grid-cols-3"
  >
    <ul class="lg:flex lg:items-center lg:w-full lg:space-x-10 lg:col-span-2">
      <li
        v-for="nav in navs"
        :key="nav.name"
        class="text-lg font-medium text-gray-300"
      >
        <nuxt-link :to="nav.url">{{ nav.name }}</nuxt-link>
      </li>
    </ul>
    <div class="relative lg:col-span-1">
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
  </nav>
</template>

<script>
export default {
  props: {
    navs: {
      type: Array,
      default: () => [],
    },
  },
  data: () => ({
    search: '',
  }),
}
</script>

<style></style>
