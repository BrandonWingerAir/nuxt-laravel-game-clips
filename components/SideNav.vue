<template>
  <div
    id="SideNav"
    :class="route.fullPath === '/' ? 'lg:w-[310px]' : 'lg:w-[220px]'"
    class="fixed x-20 bg-[#fafafa] pt-[85px] h-full lg:border-r-0 border-r w-[87px] md:w-[90px] overflow-auto"
  >
    <h2 class="lg:text-xl font-semibold md:font-lg mb-5 text-center px-4">Gaming Footage</h2>
    <hr class="mb-7 border-neutral-200 mx-auto" width="80%">
    <div class="lg:w-full w-[55px] mx-auto">
      <NuxtLink to="/">
        <MenuItem menuItemIcon="New Clips" class="bg-neutral-200" menuItemColor="#000" menuItemSize="30"/>
      </NuxtLink>
      <MenuItem menuItemIcon="Your Feed" menuItemColor="#000000" menuItemSize="27"/>
      <MenuItem menuItemIcon="Top Clips" menuItemColor="#000000" menuItemSize="27"/>
    </div>
  </div>
</template>

<script setup>
const route = useRoute();
</script>
