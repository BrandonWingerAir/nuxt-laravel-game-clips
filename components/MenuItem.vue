<template>
  <div class="w-full flex items-center hover:bg-gray-100 p-2.5 rounded-md">
    <div class="flex items-center lg:mx-0 mx-auto">
      <Icon :name="icon" :color="menuItemColor" :size="menuItemSize"/>

      <span 
        :class="`text-[${menuItemColor}]`"
        class="lg:block hidden pl-[9px] mt-0.5 font-semibold text-[17px]"
      >
        {{ menuItemIcon }}
      </span>
    </div>
  </div>
</template>

<script setup>
const props = defineProps(['menuItemIcon', 'menuItemColor', 'menuItemSize']);
const { menuItemIcon, menuItemColor, menuItemSize } = toRefs(props);

let icon = ref('');

if (menuItemIcon.value === 'New Clips') icon.value = 'la:play-circle-solid';
if (menuItemIcon.value === 'Your Feed') icon.value = 'la:newspaper-solid';
if (menuItemIcon.value === 'Top Clips') icon.value = 'la:trophy';
</script>
