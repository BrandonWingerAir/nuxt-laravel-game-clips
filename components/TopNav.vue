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
          placeholder="Search..."
        />
        <div class="px-3 py-1 flex items-center border-l border-l-grey-300">
          <Icon name="ri:search-line" color="A#A2A7" size="22"/>
        </div>
      </div>
      
      <div class="flex items-center justify-end gap-3 min-w-[275px] max-w-[320px] w-full">
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
          <Icon class="ml-1 mr-4" name="material-symbols:notifications-unread-outline" color="#161724" size="30"/>
          <Icon class="mr-5" name="bx:message-detail" color="#161724" size="27"/>
          <div class="relative">
            <button 
              class="mt-1"
              @click="$event => showMenu = !showMenu"
            >
              <img
                class="rounded-full"
                width="33"
                src="https://picsum.photos/id/83/300/320"
              />
            </button>

            <div
              v-if="showMenu"
              id="PopupMenu"
              class="absolute bg-white roudned-lg py-1.5 w-[200px] shadow-xl border top-[43px] -right-2"
            >
              <NuxtLink
                @click="$event => showMenu = false"
                class="flex items-center justify-start py-3 px-2 hover:bg-gray-100 cursor-pointer"
              >
                <Icon name="ph:user" size="20"/>
                <span class="pl-2 font-semibold text-sm">
                  Profile
                </span>
              </NuxtLink>
              <div
                class="flex items-center justify-start py-3 px-1.5 hover:bg-gray-100 border-t cursor-pointer"
              >
                <Icon name="ic:outline-login" size="20"/>
                <span class="pl-2 font-semibold text-sm">
                  Log out
                </span>
              </div>
            </div>
          </div>
        </div>
        
        <div class="flex items-center">
          <button class="flex items-center bg-[#642cf0] text-white border rounded-md px-3 py-[6px]">
            <Icon name="mdi:plus" color="white" size="25"/>
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
