<template>
  <div
    id="SideNav"
    :class="route.fullPath === '/' ? 'lg:w-[310px]' : 'lg:w-[220px]'"
    class="fixed x-20 bg-white pt-[70px] h-full lg:border-r-0 border-r w-[75px] overflow-auto"
  >
    <div class="lg:w-full w-[55px] mx-auto">
      <NuxtLink to="/">
        <MenuItem menuItemIcon="New Clips" menuItemColor="#F02C56" menuItemSize="30"/>
      </NuxtLink>
      <MenuItem menuItemIcon="Your Feed" menuItemColor="#000000" menuItemSize="27"/>
      <MenuItem menuItemIcon="Top Clips" menuItemColor="#000000" menuItemSize="27"/>
    </div>
  </div>
</template>

<script setup>
const route = useRoute();
</script>
