<template>
  <div class="flex items-center justify-between pb-5">
    <span class="text-gray-100 material-icons"> home </span>
    <div class="flex items-center space-x-4">
      <span class="text-gray-100 material-icons"> notifications </span>
      <img
        class="w-8 h-8 rounded-full"
        :src="require(`~/assets/images/${profileImg}.png`)"
        alt=""
      />
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    profileImg: 'stef',
  }),
}
</script>

<style></style>
