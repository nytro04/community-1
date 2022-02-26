<template>
  <nav
    class="grid grid-cols-1 py-6 border-t border-white gap-x-10 border-opacity-30 md:grid-cols-3"
  >
    <ul class="flex items-center w-full col-span-2 space-x-10">
      <li
        v-for="nav in navs"
        :key="nav.name"
        class="text-lg font-medium text-gray-300"
      >
        <nuxt-link :to="nav.url">{{ nav.name }}</nuxt-link>
      </li>
    </ul>
    <div class="relative col-span-1">
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
  data: () => ({
    navs: [
      { name: 'Home', url: '/home' },
      { name: 'Profile', url: '/profile' },
      { name: 'Resources', url: '/resources' },
      { name: 'Company Directory', url: '/company-directory' },
      { name: 'Openings', url: '/openings' },
    ],
  }),
}
</script>

<style></style>
