<template>
  <div
    id="SideNav"
    :class="route.fullPath === '/' ? 'lg:w-[310px]' : 'lg:w-[220px]'"
    class="fixed x-20 bg-[#fafafa] pt-[65px] h-full border border-neutral-400 w-[87px] md:w-[90px] overflow-auto"
  >
    <div class="bg-white py-5 border-b border-b-neutral-300">
      <h2 class="lg:text-xl font-semibold md:font-lg text-center px-4">
        GAMING VIDEOS
      </h2>
    </div>

    <div class="lg:w-full w-[55px] mx-auto">
      <NuxtLink to="/">
        <MenuItem menuItemIcon="New Clips" class="bg-neutral-200" menuItemColor="#000" menuItemSize="30"/>
      </NuxtLink>
      <MenuItem menuItemIcon="Your Feed" menuItemColor="#000000" menuItemSize="27"/>
      <MenuItem menuItemIcon="Top Clips" menuItemColor="#000000" menuItemSize="27"/>

      <hr width="90%" class="border-0 border-b mx-auto mt-2"/>

      <div class="lg:block hidden text-xs text-gray-600 font-semibold pt-4 pb-2 px-2">
        Suggested Accounts
      </div>

      <div class="lg:hidden block pt-3"></div>

      <div class="cursor-pointer">
        <MenuItemFollow/>
      </div>
    </div>
  </div>
</template>

<script setup>
const route = useRoute();
</script>
