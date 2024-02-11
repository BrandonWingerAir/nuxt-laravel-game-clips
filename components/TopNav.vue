<template>
  <div
    id="TopNav"
    class="fixed bg-white z-30 flex items-center w-full border-b h-[61px]"
  >
    <div
      :class="route.fullPath === '/' ? 'max-w-[1150px]' : ''"
      class="flex items-center jsutify-between w-full px-6 mx-auto"
    >
      <div :class="route.fullPath === '/' ? 'w-[80%]' : 'lg:w-[20%] w-[70%]'">
        <NuxtLink to="/" class="flex items-center">
          <img width="47" class="mr-2" src="~/assets/images/gameclips-logo.svg">
          <h1 class="mb-1 uppercase text-4xl">
            G<span class="text-lg">ame</span><span class="text-lg font-semibold">Clips</span>
          </h1>
        </NuxtLink>
      </div>

      <div class="hidden md:flex items-center bg=[#F1F1F2] p-1 rounded-full max-w-[380px] w-full">
        <input
          type="text"
          class="w-full pl-3 my-2 bg-transparent placeholder-[#838383] text-[15px] focus:outline-none"
          placeholder="Search accounts"
        />
        <div class="px-3 py-1 flex items-center border-l border-l-grey-300">
          <Icon name="ri:search-line" color="A#A2A7" size="22"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
  const route = useRoute()
</script>
