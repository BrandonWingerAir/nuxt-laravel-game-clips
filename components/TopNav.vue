<template>
  <div id="TopNav" class="fixed z-30 flex items-center w-full bg-[#212d55] border-b h-[70px]">
    <div
      :class="route.fullPath === '/' ? 'max-w-[1150px]' : ''"
      class="flex items-center justify-between w-full px-6 mx-auto"
    >
      <div :class="route.fullPath === '/' ? 'md:w-[80%] w-[30%]' : 'lg:w-[20%] w-[70%]'" class="flex md:min-w-[80%]">
        <NuxtLink to="/" class="flex items-center mr-6 text-white">
          <img width="45" class="mr-2 mb-1" src="~/assets/images/gameclips-logo.svg">
          <h1 class="mb-1 uppercase text-3xl">
            G<span class="text-lg">ame</span><span class="text-lg font-semibold">Clips</span>
          </h1>
        </NuxtLink>
        
        <div class="hidden md:flex items-center max-w-[380px] w-full">
          <input
            type="text"
            class="w-full pl-3 py-2 bg-white placeholder-neutral-500 text-[15px] border-l-2 rounded-l-full focus:outline-none"
            placeholder="Search..."
          />
          <div class="pl-3 pr-5 py-2 flex items-center bg-neutral-600 border-l border-l-grey-300 rounded-r-full">
            <Icon name="ri:search-line" color="white" size="22"/>
          </div>
        </div>
      </div>

      
      <div class="flex items-center justify-end gap-3 lg:min-w-[275px] max-w-[320px] w-full">
        <!-- <button v-if="false" class="flex items-center border rounded-sm px-3 py-[6px] hover:bg-gray-100">
          <Icon name="mdi:plus" color="#000000" size="22"/>
          <span class="px-2 font-medium text-[15px]">
            Upload
          </span>
        </button> -->

        <!-- <div class="flex items-center">
          <button class="flex items-center bg-[#642cf0] text-white border rounded-md px-3 py-[6px]">
            <span class="mx-4 font-medium text-[15px]">
              Log in
            </span>
          </button>
          <Icon name="" color="#161724" size="25"/>
        </div> -->

        <div class="flex items-center">
          <Icon class="ml-1 mr-4 text-neutral-200" size="27" name="bx:message-detail"/>
          <Icon class="mr-5" color="#ffc107" size="30" name="material-symbols:notifications-unread-outline"/>

          <div class="relative">
            <button class="mt-1 mr-2" @click="$event => showMenu = !showMenu">
              <img
                class="rounded-full"
                width="33"
                src="https://picsum.photos/id/83/300/320"
              />
            </button>

            <div v-if="showMenu" id="PopupMenu" class="absolute bg-white roudned-lg py-1.5 w-[200px] shadow-xl border top-[43px] -right-2">
              <NuxtLink @click="$event => showMenu = false" class="flex items-center justify-start py-3 px-2 hover:bg-gray-100 cursor-pointer">
                <Icon name="ph:user" size="20"/>
                <span class="pl-2 font-semibold text-sm">
                  Profile
                </span>
              </NuxtLink>

              <div class="flex items-center justify-start py-3 px-1.5 hover:bg-gray-100 border-t cursor-pointer">
                <Icon name="ic:outline-login" size="20"/>
                <span class="pl-2 font-semibold text-sm">
                  Log out
                </span>
              </div>
            </div>
          </div>
        </div>
        
        <div class="flex items-center text-white hidden lg:flex">
          <button class="flex items-center bg-emerald-600 border border-slate-400 rounded-md px-3 py-[6px]">
            <Icon name="mdi:plus" size="25"/>
            <span class="px-2 font-medium text-[15px]">
              Upload
            </span>
          </button>
        </div>

      </div>
    </div>
  </div>
</template>

<script setup>
  const route = useRoute();
  let showMenu = ref(false);
</script>
