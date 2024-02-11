<template>
  <div
    id="SideNav"
    :class="rout.fullPath === '/' ? 'lg:w-[310px]' : 'lg:w-[220px]'"
    class="fixed x-20 bg-white pt-[70px] h-full lg:border-r-0 border-r w-[75px] overflow-auto"
  >
    <div class="lg:w-full w-[55px] mx-auto">
      <NuxtLink iconString="For You"/>
    </div>
  </div>
</template>

<script setup>
const route = useRoute();
</script>
